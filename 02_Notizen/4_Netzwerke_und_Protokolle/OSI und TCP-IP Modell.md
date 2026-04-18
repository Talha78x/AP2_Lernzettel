# OSI und TCP-IP Modell

## Definition
Das **OSI-Modell** ist ein Referenzmodell mit **7 Schichten**, das Netzwerkkommunikation logisch strukturiert. Das **TCP/IP-Modell** ist das praxisnahe Modell des Internets und wird meist mit **4 Schichten** beschrieben.

Beide Modelle helfen dabei, Netzwerkfunktionen sauber einzuordnen und Fehler systematisch zu lokalisieren.

## Warum ist das so?
Kommunikation im Netzwerk besteht aus vielen Teilaufgaben:
- elektrische oder optische Übertragung
- Adressierung im lokalen Netz
- Routing zwischen Netzen
- Ende-zu-Ende-Kommunikation
- Anwendungsprotokolle wie HTTP oder SMTP

Ohne Schichtenmodell würde alles vermischt werden. Mit Schichten kann man sauber trennen, standardisieren und Fehler einfacher eingrenzen.

## Zusammenspiel
- [[Standardprotokolle (TCP, UDP, MAC, ARP, ICMP, HTTP, HTTPS, FTP, SMTP...)]] lassen sich den Schichten zuordnen.
- [[IPv4 (Grundlagen & Subnetting usw..)]] und [[IPv6 (Grundlagen & Subnetting usw..)]] arbeiten auf Schicht 3.
- [[TLS & SSL]] liegt oberhalb von TCP und schützt Anwendungsdaten.
- [[VLAN (Arten, Trunking ...)]] und [[Spanning Tree]] betreffen vor allem Schicht 2.
- [[Routing (statisch, dynamisch, Inter-VLAN, Protokolle wie OSPF, RIP, BGP)]] ist ein Schicht-3-Thema.

## Eigene Worte (prüfungsnah)
Das OSI-Modell ist wie ein Stapel von Aufgaben. Jede Schicht hat eine eigene Verantwortung und nutzt die darunterliegende Schicht. So kann man bei einem Fehler gezielt fragen: Liegt das Problem am Kabel, an der MAC-Kommunikation, an der IP-Adressierung, am Transport oder an der Anwendung?

## OSI-Schichten
| Schicht | Name | Aufgabe | Beispiele |
|---|---|---|---|
| 7 | Anwendung | Dienste für Anwendungen | HTTP, SMTP, DNS |
| 6 | Darstellung | Format, Kodierung, Verschlüsselung | TLS, Zeichensätze |
| 5 | Sitzung | Sitzungssteuerung | Verbindungssteuerung zwischen Anwendungen |
| 4 | Transport | Ende-zu-Ende-Transport, Ports | TCP, UDP |
| 3 | Vermittlung | logische Adressierung, Routing | IPv4, IPv6, ICMP |
| 2 | Sicherung | Frames, MAC-Adressen, Fehlererkennung | Ethernet, MAC, VLAN |
| 1 | Bitübertragung | Signale, Kabel, Funk | Kupfer, Glasfaser, WLAN-Signal |

## TCP/IP-Modell
| TCP/IP-Schicht | Entspricht grob OSI | Beispiele |
|---|---|---|
| Anwendung | OSI 5-7 | HTTP, DNS, SMTP, FTP |
| Transport | OSI 4 | TCP, UDP |
| Internet | OSI 3 | IP, ICMP |
| Netzzugang | OSI 1-2 | Ethernet, WLAN, MAC |

## Warum nutzt man in Prüfungen oft beide Modelle?
| Modell | Stärke |
|---|---|
| OSI | sehr gut zum Lernen, Strukturieren und Eingrenzen |
| TCP/IP | näher an der echten Internetpraxis |

Darum lautet eine typische Prüfungsantwort:
"Das OSI-Modell ist ein Referenzmodell zur Einordnung, das TCP/IP-Modell beschreibt die praktisch verwendete Protokollfamilie."

## Kapselung im Zusammenspiel
Beim Senden werden Daten schrittweise "verpackt":
1. Die Anwendung erzeugt Daten, zum Beispiel einen HTTP-Request.
2. TCP ergänzt Ports und Kontrollinformationen.
3. IP ergänzt Quell- und Ziel-IP.
4. Ethernet ergänzt Quell- und Ziel-MAC.
5. Die Bits werden über Kabel, Funk oder Glasfaser übertragen.

Beim Empfänger wird das Ganze in umgekehrter Reihenfolge entpackt. Das nennt man **Dekapselung**.

## Beispielaufgabe mit Lösung
**Aufgabe:** Ein Client ruft `https://example.org` auf. Ordne die folgenden Begriffe einer OSI-Schicht zu: `MAC-Adresse`, `TCP`, `IPv4`, `HTTPS`.

**Lösung:**
- `MAC-Adresse` -> **Schicht 2**
- `TCP` -> **Schicht 4**
- `IPv4` -> **Schicht 3**
- `HTTPS` -> **Schicht 7** im Prüfungsalltag, technisch mit TLS-Bezug zu Schicht 6/7

**Wichtig:**
In vielen IHK-Aufgaben wird HTTPS pragmatisch der Anwendungsschicht zugeordnet. TLS wird je nach Darstellung Schicht 6 oder 7-nah eingeordnet.

## Typische Prüfungsszenarien
- Schichten und Protokolle korrekt zuordnen.
- OSI und TCP/IP voneinander abgrenzen.
- Kapselung und Dekapselung erklären.
- Fehler eingrenzen, zum Beispiel "Ping geht, aber Webseite nicht".

## Merksätze
- Schicht 2 kennt MAC, Schicht 3 kennt IP, Schicht 4 kennt Ports.
- OSI ist das Lernmodell, TCP/IP das Praxismodell.
- Gute Fehlersuche arbeitet sich schichtweise vor.
