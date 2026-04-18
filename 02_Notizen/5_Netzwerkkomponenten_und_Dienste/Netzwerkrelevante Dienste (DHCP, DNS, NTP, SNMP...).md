# Netzwerkrelevante Dienste (DHCP, DNS, NTP, SNMP...)

## Definition
Netzwerkrelevante Dienste sind grundlegende Infrastrukturdienste, ohne die moderne Netze nur eingeschränkt oder gar nicht funktionieren. Besonders wichtig sind:

- **DHCP** für automatische IP-Konfiguration
- **DNS** für Namensauflösung
- **NTP** für Zeitsynchronisation
- **SNMP** für Überwachung und Verwaltung

## Warum ist das so?
Ein Netzwerk braucht mehr als nur Kabel und IP-Adressen:
- Clients brauchen automatisch gültige Netzwerkeinstellungen
- Namen müssen in IP-Adressen übersetzt werden
- Systeme brauchen eine gemeinsame Uhrzeit
- Geräte und Dienste müssen überwacht werden

Wenn diese Dienste fehlen oder falsch arbeiten, treten oft schwer erkennbare Folgefehler auf.

## Zusammenspiel
- [[IPv4 (Grundlagen & Subnetting usw..)]] und [[IPv6 (Grundlagen & Subnetting usw..)]] liefern die Adressbasis.
- [[URLs und DNS]] vertieft die DNS-Seite fachlich.
- [[Active Directory und LDAP]] ist in Windows-Umgebungen besonders eng mit DNS und NTP verknüpft.
- [[Monitoring und SNMP]] behandelt SNMP vertieft.
- [[Netzwerkkomponenten]] zeigt, auf welchen Systemen diese Dienste typischerweise laufen.

## Eigene Worte (prüfungsnah)
DHCP gibt einem Client seine Netzwerkkarte "die Grundausstattung", DNS übersetzt Namen, NTP hält alle Uhren gleich und SNMP sorgt dafür, dass Administratoren den Zustand von Geräten überwachen können.

## DHCP
**DHCP (Dynamic Host Configuration Protocol)** verteilt automatisch:
- IP-Adresse
- Subnetzmaske
- Standardgateway
- DNS-Server

### DORA-Ablauf
| Schritt | Bedeutung |
|---|---|
| Discover | Client sucht DHCP-Server |
| Offer | Server bietet Konfiguration an |
| Request | Client fordert ein Angebot an |
| Acknowledge | Server bestätigt die Zuweisung |

**Typische Ports:** UDP 67/68

## DNS
**DNS (Domain Name System)** übersetzt Namen in IP-Adressen und umgekehrt.

| Record-Typ | Bedeutung |
|---|---|
| A | Name zu IPv4-Adresse |
| AAAA | Name zu IPv6-Adresse |
| MX | Mailserver |
| CNAME | Alias |
| PTR | Reverse Lookup |

**Typischer Port:** 53 UDP/TCP

## NTP
**NTP (Network Time Protocol)** synchronisiert die Uhrzeit von Systemen.

Warum wichtig?
- Logs müssen zeitlich zusammenpassen
- Zertifikate brauchen korrekte Zeit
- Authentifizierungsverfahren wie Kerberos reagieren empfindlich auf Zeitabweichung

**Typischer Port:** 123 UDP

## SNMP
**SNMP (Simple Network Management Protocol)** dient der Überwachung und Verwaltung von Geräten.

Typische Einsätze:
- Status von Switches und Routern abfragen
- Interfaces überwachen
- Warnungen und Traps empfangen

**Typische Ports:** 161/162 UDP

## Dienste im Vergleich
| Dienst | Kernaufgabe | Auswirkung bei Ausfall |
|---|---|---|
| DHCP | automatische Netzkonfiguration | neue Clients bekommen oft keine gültige Konfiguration |
| DNS | Namensauflösung | Dienste per Namen schwer oder nicht erreichbar |
| NTP | gleiche Uhrzeit | Logs, Kerberos, Zertifikate problematisch |
| SNMP | Monitoring | fehlende Transparenz und Warnmeldungen |

## Beispielaufgabe mit Lösung
**Aufgabe:** Ein neuer PC erhält automatisch eine IP-Adresse, kann aber Webseiten nur per IP und nicht per Name erreichen. Welcher Dienst ist wahrscheinlich gestört?

**Lösung:**
Wahrscheinlich **DNS**.

**Begründung:**
1. Die IP-Konfiguration funktioniert bereits, also arbeitet DHCP grundsätzlich.
2. Wenn nur Namen nicht aufgelöst werden, ist die Namensauflösung das Problem.
3. Webseitenaufruf per IP zeigt, dass die reine Netzverbindung vorhanden ist.

## Typische Prüfungsszenarien
- DORA-Reihenfolge angeben.
- DNS-Record-Typen zuordnen.
- erklären, warum NTP für Kerberos und Zertifikate wichtig ist.
- DHCP und DNS in Fehlerszenarien unterscheiden.

## Merksätze
- DHCP gibt Konfiguration, DNS gibt Orientierung, NTP gibt Zeit.
- DNS-Probleme sehen oft wie "Internet kaputt" aus, obwohl die Verbindung steht.
- Ohne saubere Zeit können viele Sicherheitsmechanismen scheitern.
