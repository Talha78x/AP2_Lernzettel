# VPN (Tunneling, standortübergreifende Kommunikation)

## Definition
Ein **VPN (Virtual Private Network)** verbindet Benutzer oder Standorte sicher über ein unsicheres Netz wie das Internet. Die Kommunikation läuft dabei durch einen **geschützten Tunnel**.

Ein VPN macht aus dem Internet kein privates Netz, sondern baut eine logisch geschützte Verbindung über ein öffentliches Netz.

## Warum ist das so?
Unternehmen müssen oft:
- Außenstellen verbinden
- Homeoffice-Zugriffe ermöglichen
- Daten sicher über öffentliche Netze transportieren

Ohne zusätzliche Schutzmechanismen könnten Inhalte mitgelesen oder manipuliert werden. VPNs schaffen deshalb Vertraulichkeit, Integrität und Authentizität auf dem Transportweg.

## Zusammenspiel
- [[TLS & SSL]] ist ein alternatives bzw. ergänzendes Sicherheitsprinzip auf höherer Ebene.
- [[NAT & PAT]] kann VPN-Verbindungen beeinflussen, weil Adressübersetzung und Tunnel zusammenspielen müssen.
- [[OSI und TCP-IP Modell]] hilft bei der Einordnung von IPsec oder SSL-/TLS-VPNs.
- [[Zertifikate]] und [[Hashverfahren & digitale Signaturen]] sind für Authentifizierung und Vertrauensprüfung wichtig.
- [[Routing (statisch, dynamisch, Inter-VLAN, Protokolle wie OSPF, RIP, BGP)]] ist nötig, damit Daten durch den Tunnel zu den richtigen Zielnetzen gelangen.

## Eigene Worte (prüfungsnah)
Ein VPN ist wie ein geschützter Rohrpostkanal durch ein unsicheres Gebiet. Außen sieht man nur, dass zwei Endpunkte miteinander kommunizieren. Der eigentliche Inhalt im Tunnel bleibt geschützt.

## Typische VPN-Arten
| Art | Einsatz | Beispiel |
|---|---|---|
| Site-to-Site-VPN | Standort zu Standort | Hauptsitz mit Außenstelle verbinden |
| Remote-Access-VPN | Benutzer zu Firmennetz | Homeoffice-Zugriff |
| Client-to-Site-VPN | einzelner Rechner zum Unternehmensgateway | Laptop eines Mitarbeiters |

## Was bedeutet Tunneling?
Beim **Tunneling** wird ein ursprüngliches Paket in ein neues Paket eingebettet:
- inneres Paket: eigentliche Nutzdaten
- äußeres Paket: Transport durch das öffentliche Netz

Dadurch sind interne Adressen und Inhalte nach außen abgeschirmt.

## IPsec im Überblick
**IPsec** arbeitet auf Schicht 3 und ist besonders wichtig für Standortvernetzung.

| Baustein | Aufgabe |
|---|---|
| AH | Authentizität und Integrität, aber keine Verschlüsselung |
| ESP | Verschlüsselung plus Integrität/Authentizität |
| IKE | Schlüsselaustausch und Aufbau der Sicherheitsbeziehung |

In der Praxis ist **ESP** deutlich relevanter als AH.

## VPN und TLS unterscheiden
| Punkt | VPN / IPsec | TLS |
|---|---|---|
| Schutzebene | netznah, meist Schicht 3 | anwendungsnah |
| Einsatz | ganze Netze oder Benutzerzugang | einzelne Dienste wie HTTPS |
| Sicht auf Anwendungen | meist transparent | an konkrete Anwendungen gekoppelt |

## Beispiel: Standortkopplung
Ein Unternehmen hat:
- Standort A: `192.168.10.0/24`
- Standort B: `192.168.20.0/24`

Ein Site-to-Site-VPN sorgt dafür, dass Rechner beider Netze sicher kommunizieren können, obwohl die Verbindung über das Internet läuft.

## Beispielaufgabe mit Lösung
**Aufgabe:** Zwei Firmenstandorte sollen so verbunden werden, dass interne Server an beiden Standorten sicher erreichbar sind. Welcher VPN-Typ ist am passendsten?

**Lösung:**
Ein **Site-to-Site-VPN**.

**Begründung:**
1. Es geht nicht nur um einen einzelnen Benutzer, sondern um ganze Netze.
2. Beide Standorte sollen dauerhaft gekoppelt werden.
3. Das ist der klassische Anwendungsfall für IPsec-basierte Standortvernetzung.

## Typische Prüfungsszenarien
- VPN erklären, ohne es mit HTTPS zu verwechseln.
- Site-to-Site und Remote Access unterscheiden.
- Tunneling in eigenen Worten beschreiben.
- IPsec und TLS gegeneinander abgrenzen.
- Schutzziele eines VPN nennen.

## Merksätze
- VPN heißt nicht "privates Internet", sondern "geschützter Tunnel".
- Site-to-Site verbindet Netze, Remote Access verbindet Benutzer.
- IPsec ist der Klassiker für Standortkopplung.
- TLS schützt meist einzelne Anwendungen, VPN schützt oft ganze Verkehrswege.
