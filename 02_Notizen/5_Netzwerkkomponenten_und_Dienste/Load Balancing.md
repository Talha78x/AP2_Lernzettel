# Load Balancing

## Definition
**Load Balancing** verteilt eingehende Anfragen oder Verbindungen auf mehrere Server oder Instanzen. Ziel ist, Last zu verteilen, Überlastungen zu vermeiden und die Verfügbarkeit zu erhöhen.

## Warum ist das so?
Wenn alle Anfragen auf nur einem Server landen, entstehen schnell Probleme:
- Überlastung
- langsamere Antwortzeiten
- Ausfall bei Hardware- oder Softwarefehlern

Mit mehreren Servern kann ein Dienst stabiler und skalierbarer bereitgestellt werden.

## Zusammenspiel
- [[Snap-Shot, Versionierung, Hochverfügbarkeit (Clustering, Load Balancing, FHRP)]] ordnet Load Balancing in Hochverfügbarkeit ein.
- [[Netzwerkkomponenten]] liefert den technischen Kontext zu Reverse Proxies und Appliances.
- [[TLS & SSL]] ist relevant, wenn ein Load Balancer HTTPS terminiert.
- [[Firewall (IDS, IPS, DMZ, ACL, Filtertabelle)]] spielt oft an denselben Netzgrenzen eine Rolle.
- [[2-Tier-, 3-Tier- und Multi-Tier-Architekturen]] ergänzt die Architekturperspektive.

## Eigene Worte (prüfungsnah)
Ein Load Balancer ist der Verteiler vor mehreren Servern. Er entscheidet, welcher Server die nächste Anfrage bekommt, damit nicht alle Last auf einem einzigen System landet.

## Ziele von Load Balancing
| Ziel | Bedeutung |
|---|---|
| Lastverteilung | Anfragen auf mehrere Systeme verteilen |
| Skalierbarkeit | mehr Kapazität durch zusätzliche Server |
| Verfügbarkeit | Ausfall einzelner Server besser abfangen |
| Wartbarkeit | Systeme im laufenden Betrieb austauschbar machen |

## Typische Verfahren
| Verfahren | Funktionsweise | Typischer Nutzen |
|---|---|---|
| Round Robin | Anfragen reihum verteilen | einfach, gleichmäßige Verteilung |
| Least Connections | Ziel mit wenigsten aktiven Verbindungen | gut bei unterschiedlich langer Last |
| Weighted Round Robin | Server mit Gewichtung bevorzugen | unterschiedlich starke Server |
| IP Hash | gleicher Client landet oft wieder auf gleichem Ziel | Session-Persistenz |

## Layer 4 vs. Layer 7
| Ebene | Arbeitsweise | Beispiel |
|---|---|---|
| Layer 4 | verteilt nach IP und Port | TCP-Verbindungen auf Webserver |
| Layer 7 | versteht Anwendungsdaten | `/api` auf API-Cluster, `/shop` auf Shop-Server |

## Health Checks
Ein guter Load Balancer prüft regelmäßig, ob ein Zielserver gesund ist.

Typische Prüfungen:
- Port erreichbar?
- HTTP-Status korrekt?
- Antwortzeit akzeptabel?

Nur gesunde Server sollten neue Anfragen erhalten.

## Beispielaufgabe mit Lösung
**Aufgabe:** Ein Webshop soll auch dann erreichbar bleiben, wenn einer von drei Webservern ausfällt. Welche Komponente ist sinnvoll?

**Lösung:**
Ein **Load Balancer** vor den Webservern.

**Begründung:**
1. Anfragen werden auf mehrere Server verteilt.
2. Fällt ein Server aus, können die anderen weiterarbeiten.
3. Mit Health Checks kann der defekte Server automatisch aus der Verteilung genommen werden.

## Typische Prüfungsszenarien
- Load Balancing von FHRP unterscheiden.
- Layer 4 und Layer 7 abgrenzen.
- Round Robin und Least Connections vergleichen.
- Session-Persistenz erklären.
- Health Checks begründen.

## Merksätze
- Load Balancing verteilt Last, FHRP sichert das Gateway.
- Mehr Server bedeuten ohne Verteilinstanz noch keine gute Skalierung.
- Ein Load Balancer erhöht Verfügbarkeit nur dann sauber, wenn Zielsysteme überwacht werden.
