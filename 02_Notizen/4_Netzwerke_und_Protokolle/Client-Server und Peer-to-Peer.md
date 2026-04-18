# Client-Server und Peer-to-Peer

## Definition
**Client-Server** und **Peer-to-Peer (P2P)** sind zwei grundlegende Kommunikationsmodelle in Netzwerken.

- Beim **Client-Server-Modell** stellt ein zentraler Server Dienste, Daten oder Ressourcen bereit. Clients greifen gezielt darauf zu.
- Beim **Peer-to-Peer-Modell** sind die Teilnehmer gleichberechtigt. Jeder Peer kann gleichzeitig Anbieter und Nutzer von Ressourcen sein.

## Warum ist das so?
Netzwerke müssen klären, **wer welche Rolle hat**:
- Wer speichert Daten dauerhaft?
- Wer authentifiziert Benutzer?
- Wer beantwortet Anfragen?
- Wer darf ausfallen, ohne dass alles stillsteht?

Je nach Ziel ist ein zentrales oder dezentrales Modell sinnvoller. Unternehmen setzen meist auf zentrale Steuerung, während dezentrale Systeme auf Verteilung und Ausfallsicherheit setzen.

## Zusammenspiel
- [[OSI und TCP-IP Modell]] erklärt, auf welchen Schichten die Kommunikation technisch stattfindet.
- [[Standardprotokolle (TCP, UDP, MAC, ARP, ICMP, HTTP, HTTPS, FTP, SMTP...)]] liefern die Regeln für diese Kommunikation.
- [[Netzwerkrelevante Dienste (DHCP, DNS, NTP, SNMP...)]] sind meist klassische Client-Server-Dienste.
- [[Active Directory und LDAP]] ist ein typisches Beispiel für zentrale Serverdienste.
- P2P taucht in verteilten Systemen, Dateitausch oder Blockchain-Konzepten auf.

## Eigene Worte (prüfungsnah)
Client-Server bedeutet: Einer dient, viele fragen an. P2P bedeutet: Alle können beides. Der große Unterschied liegt also nicht im Kabel oder Protokoll, sondern in der Rollenverteilung und Verwaltung.

## Gegenüberstellung
| Merkmal | Client-Server | Peer-to-Peer |
|---|---|---|
| Rollen | klar getrennt | gleichberechtigt |
| Verwaltung | zentral | dezentral |
| Datensicherung | einfacher | aufwendiger |
| Skalierung | gut planbar | abhängig von Peers |
| Ausfallrisiko | Server kann Single Point of Failure sein | kein zentraler Ausfallpunkt |
| Sicherheit | leichter zentral durchsetzbar | schwerer einheitlich steuerbar |

## Typische Beispiele
| Szenario | Modell | Warum? |
|---|---|---|
| Webanwendung mit Datenbank | Client-Server | Browser fragt Server an |
| Dateiserver im Unternehmen | Client-Server | zentrale Rechte und Backups |
| BitTorrent | Peer-to-Peer | viele Teilnehmer teilen Daten direkt |
| Blockchain-Netzwerk | Peer-to-Peer | kein zentraler Hauptserver |

## Vorteile und Nachteile
### Client-Server
**Vorteile:**
- zentrale Benutzer- und Rechteverwaltung
- einfachere Wartung
- kontrollierte Backups
- klare Sicherheitsrichtlinien

**Nachteile:**
- Serverausfall betrifft viele Nutzer
- leistungsfähige Serverhardware nötig
- zentrale Komponenten werden zum kritischen Punkt

### Peer-to-Peer
**Vorteile:**
- keine zwingende Zentralinstanz
- gute Lastverteilung möglich
- einzelne Ausfälle sind oft weniger kritisch

**Nachteile:**
- schwieriger zu administrieren
- uneinheitliche Sicherheitslage
- Datenkonsistenz und Backup komplizierter

## Beispielaufgabe mit Lösung
**Aufgabe:** Ein Unternehmen möchte Benutzer zentral verwalten, Zugriffe protokollieren und tägliche Datensicherungen auf einem Fileserver durchführen. Welches Modell ist geeigneter?

**Lösung:**
Geeignet ist das **Client-Server-Modell**.

**Begründung:**
1. Benutzer und Rechte sollen zentral verwaltet werden.
2. Daten sollen an einer kontrollierten Stelle gespeichert werden.
3. Backups und Protokollierung sind mit zentralem Server deutlich einfacher.

**Prüfungsfalle:**
P2P ist nicht automatisch "moderner" oder "besser". Für Unternehmensnetze ist zentrale Verwaltung meist wichtiger als maximale Dezentralität.

## Typische Prüfungsszenarien
- Client-Server und P2P gegeneinander abgrenzen.
- Vor- und Nachteile für Unternehmen nennen.
- Single Point of Failure beim Client-Server erklären.
- Typische Dienste wie DNS, DHCP oder Webserver korrekt zuordnen.

## Merksätze
- Client-Server bringt Kontrolle, P2P bringt Verteilung.
- In Firmennetzen dominiert meist Client-Server.
- Die Wahl des Modells beeinflusst Sicherheit, Backup und Administration direkt.
