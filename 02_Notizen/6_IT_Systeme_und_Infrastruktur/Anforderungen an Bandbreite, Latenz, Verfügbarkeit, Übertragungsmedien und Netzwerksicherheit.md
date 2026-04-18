# Anforderungen an Bandbreite, Latenz, Verfügbarkeit, Übertragungsmedien und Netzwerksicherheit

## Definition
Bei der Planung von IT-Infrastrukturen müssen technische Anforderungen bewertet werden, damit Anwendungen zuverlässig und passend betrieben werden können. Zu den wichtigsten Kriterien gehören:
- **Bandbreite**
- **Latenz**
- **Verfügbarkeit**
- **Übertragungsmedium**
- **Netzwerksicherheit**

## Warum ist das so?
Nicht jede Anwendung stellt dieselben Anforderungen:
- Backups brauchen viel Bandbreite
- VoIP braucht geringe Latenz
- Produktionssysteme brauchen hohe Verfügbarkeit
- Außenstellen brauchen sichere Verbindungen

Eine gute Infrastruktur entsteht deshalb nicht durch "möglichst viel von allem", sondern durch passende technische Entscheidungen.

## Zusammenspiel
- [[QoS]] spielt bei Latenz und Priorisierung eine große Rolle.
- [[Strukturierte Verkabelung (Kupfer, Glasfaser, Funk, WLAN und Bluetooth)]] beeinflusst Bandbreite, Reichweite und Störanfälligkeit.
- [[Server und Storage]] und [[First-Hop Redundancy Protocol (FHRP)]] unterstützen Verfügbarkeit.
- [[Firewall (IDS, IPS, DMZ, ACL, Filtertabelle)]] und [[VPN (Tunneling, standortübergreifende Kommunikation)]] sind zentrale Sicherheitsbausteine.
- [[Load Balancing]] erhöht Verfügbarkeit und Skalierung.

## Eigene Worte (prüfungsnah)
Infrastrukturplanung heißt: Ich prüfe, was eine Lösung technisch wirklich braucht. Eine große Dateiübertragung braucht andere Eigenschaften als eine Videokonferenz oder ein Domaincontroller.

## Wichtige Begriffe
| Begriff | Bedeutung | Typischer Schwerpunkt |
|---|---|---|
| Bandbreite | maximale Datenmenge pro Zeit | wichtig für große Transfers |
| Latenz | Verzögerung bis zur Ankunft | wichtig für interaktive Dienste |
| Verfügbarkeit | Anteil der nutzbaren Zeit | wichtig für kritische Systeme |
| Übertragungsmedium | technischer Transportweg | beeinflusst Reichweite, Störung, Leistung |
| Netzwerksicherheit | Schutz vor Angriff und Missbrauch | wichtig für Vertraulichkeit und Integrität |

## Typische Anforderungen nach Szenario
| Szenario | Besonders wichtig |
|---|---|
| Backup-Fenster | hohe Bandbreite |
| VoIP / Videokonferenz | geringe Latenz, wenig Jitter |
| ERP / produktive Datenbank | hohe Verfügbarkeit, stabile Antwortzeiten |
| Standortkopplung | Sicherheit, Verfügbarkeit, passende Bandbreite |
| WLAN für mobile Nutzer | Ausleuchtung, Sicherheit, Funkplanung |

## Verfügbarkeit grob einordnen
| Verfügbarkeit | ungefähre Ausfallzeit pro Jahr |
|---|---|
| 99 % | ca. 3,65 Tage |
| 99,9 % | ca. 8,76 Stunden |
| 99,99 % | ca. 52,6 Minuten |

**Wichtig:** Hohe Verfügbarkeit erfordert meist Redundanz, Überwachung und sauberes Design.

## Medienwahl
| Medium | Typischer Vorteil | Typischer Nachteil |
|---|---|---|
| Kupfer | günstig, standardisiert | begrenzte Reichweite |
| Glasfaser | hohe Reichweite und Störsicherheit | teurer, komplexer |
| Funk / WLAN | flexibel | störanfälliger, gemeinsames Medium |

## Sicherheitsanforderungen
Netzwerksicherheit umfasst zum Beispiel:
- Segmentierung
- Zugriffskontrolle
- Verschlüsselung
- sichere Authentifizierung
- Absicherung von Übergängen nach außen

## Beispielaufgabe mit Lösung
**Aufgabe:** Eine Videokonferenz-Lösung läuft trotz hoher Internetbandbreite schlecht, weil Sprache stockt und verzögert ankommt. Welcher Faktor ist wahrscheinlich kritischer als reine Bandbreite?

**Lösung:**
Die **Latenz** und oft auch **Jitter**.

**Begründung:**
Echtzeitkommunikation reagiert besonders empfindlich auf Verzögerungen und Schwankungen. Viel Bandbreite allein garantiert keine gute Gesprächsqualität.

## Typische Prüfungsszenarien
- Bandbreite und Latenz unterscheiden.
- Verfügbarkeit grob berechnen oder einordnen.
- passende Medien für Anforderungen auswählen.
- Sicherheitsanforderungen mit technischen Maßnahmen verbinden.

## Merksätze
- Viel Bandbreite ersetzt keine geringe Latenz.
- Hohe Verfügbarkeit braucht mehr als gute Hardware.
- Anforderungen müssen zur Anwendung passen, nicht umgekehrt.
