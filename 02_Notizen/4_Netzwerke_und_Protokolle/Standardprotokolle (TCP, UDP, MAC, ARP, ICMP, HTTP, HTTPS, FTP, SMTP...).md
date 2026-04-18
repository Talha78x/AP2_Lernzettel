# Standardprotokolle (TCP, UDP, MAC, ARP, ICMP, HTTP, HTTPS, FTP, SMTP...)

## Definition
**Protokolle** sind festgelegte Regeln für die Kommunikation in Netzwerken. Sie definieren, wie Daten aufgebaut, adressiert, übertragen, bestätigt und interpretiert werden.

Ohne Protokolle könnten Geräte zwar Signale senden, aber nicht verlässlich miteinander kommunizieren.

## Warum ist das so?
Netzwerkkommunikation braucht Antworten auf mehrere Fragen:
- Wer ist das Ziel?
- Auf welchem Weg werden Daten gesendet?
- Welcher Dienst ist gemeint?
- Muss die Übertragung zuverlässig oder möglichst schnell sein?
- Sollen Daten verschlüsselt werden?

Darum gibt es nicht "das eine Netzwerkprotokoll", sondern eine ganze Familie von Protokollen für unterschiedliche Schichten und Aufgaben.

## Zusammenspiel
- [[OSI und TCP-IP Modell]] hilft bei der Schichteinordnung.
- [[IPv4 (Grundlagen & Subnetting usw..)]] und [[IPv6 (Grundlagen & Subnetting usw..)]] liefern logische Adressen.
- [[TLS & SSL]] schützt viele Anwendungsprotokolle, zum Beispiel HTTPS.
- [[NAT & PAT]] arbeitet mit IP-Adressen und Ports.
- [[Client-Server und Peer-to-Peer]] beschreibt, wie Rollen im Netzwerk verteilt sind.

## Eigene Worte (prüfungsnah)
Protokolle sind die gemeinsame Sprache im Netzwerk. MAC sagt, welche Netzwerkkarte im lokalen Netz gemeint ist. IP sagt, in welches Netz etwas soll. TCP oder UDP regeln den Transport. HTTP, SMTP oder DNS definieren schließlich den eigentlichen Dienst.

## Protokolle nach Schicht
| Ebene | Protokoll / Begriff | Aufgabe |
|---|---|---|
| Schicht 2 | MAC, Ethernet | lokale Zustellung im LAN |
| Schicht 2/3 | ARP | IPv4-Adresse zu MAC auflösen |
| Schicht 3 | IP, ICMP | Routing und Kontrollmeldungen |
| Schicht 4 | TCP, UDP | Transport zwischen Anwendungen |
| Schicht 7 | HTTP, HTTPS, FTP, SMTP, DNS | Anwendungsdienste |

## TCP und UDP
| Merkmal | TCP | UDP |
|---|---|---|
| Verbindungsaufbau | ja | nein |
| Zuverlässigkeit | hoch | keine eingebaute Sicherung |
| Reihenfolge | garantiert | nicht garantiert |
| Geschwindigkeit | meist langsamer | meist schneller |
| Typische Nutzung | Web, Mail, Dateiübertragung | DNS, VoIP, Streaming |

### TCP Three-Way Handshake
1. **SYN**: Client will Verbindung aufbauen.
2. **SYN-ACK**: Server bestätigt und antwortet.
3. **ACK**: Client bestätigt.

Danach gilt die TCP-Verbindung als aufgebaut.

## Lokale Kommunikation: MAC und ARP
### MAC-Adresse
Eine **MAC-Adresse** identifiziert eine Netzwerkschnittstelle innerhalb eines lokalen Netzes.

### ARP
**ARP** fragt im IPv4-LAN:
"Welche MAC-Adresse gehört zu dieser IPv4-Adresse?"

**Ablauf:**
1. Host kennt Ziel-IP.
2. Host sendet ARP-Request als Broadcast.
3. Zielhost antwortet mit seiner MAC-Adresse.
4. Eintrag landet im ARP-Cache.

Für IPv6 gibt es statt ARP Neighbor Discovery über ICMPv6.

## ICMP
**ICMP** transportiert Steuer- und Fehlermeldungen, zum Beispiel:
- Ziel nicht erreichbar
- TTL abgelaufen
- Echo Request / Echo Reply bei `ping`

Wichtig: ICMP transportiert normalerweise keine normalen Anwendungsdaten, sondern Informationen über die Netzkommunikation selbst.

## Wichtige Anwendungsprotokolle und Ports
| Protokoll | Standardport | Typische Transportbasis | Zweck |
|---|---|---|---|
| HTTP | 80 | TCP | unverschlüsselte Webkommunikation |
| HTTPS | 443 | TCP | Webkommunikation mit TLS |
| FTP | 21 | TCP | Dateiübertragung |
| SMTP | 25 | TCP | Mailversand zwischen Servern |
| IMAP | 143 | TCP | E-Mail-Zugriff auf Server |
| POP3 | 110 | TCP | E-Mails abrufen und lokal speichern |
| DNS | 53 | UDP/TCP | Namensauflösung |
| DHCP | 67/68 | UDP | automatische IPv4-Adressvergabe |
| SSH | 22 | TCP | sicherer Fernzugriff |

## Typisches Zusammenspiel beim Webseitenaufruf
**Beispiel:** Ein Client ruft `https://example.org` auf.

1. Über [[URLs und DNS]] wird der Name in eine IP-Adresse aufgelöst.
2. Mit ARP oder Neighbor Discovery wird die lokale Ziel-MAC des nächsten Hops ermittelt.
3. TCP baut eine Verbindung auf.
4. [[TLS & SSL]] sichert die Verbindung ab.
5. HTTP überträgt die Anfrage und Antwort.

## Beispielaufgabe mit Lösung
**Aufgabe:** Nenne das passende Protokoll:
1. lokale Auflösung von IPv4 zu MAC
2. zuverlässiger Transport mit Verbindungsaufbau
3. gesicherter Webseitenzugriff
4. Versand von E-Mails

**Lösung:**
1. **ARP**
2. **TCP**
3. **HTTPS**
4. **SMTP**

## Typische Prüfungsszenarien
- TCP und UDP vergleichen.
- Protokolle einer Schicht zuordnen.
- Ports von Standarddiensten nennen.
- ARP von DNS unterscheiden.
- erklären, warum HTTPS nicht einfach nur "HTTP auf anderem Port" ist.

## Merksätze
- MAC ist lokal, IP ist logisch und netzübergreifend.
- TCP ist zuverlässig, UDP ist leichtgewichtig.
- HTTPS = HTTP plus TLS.
- DNS übersetzt Namen, ARP übersetzt IPv4 in MAC.
