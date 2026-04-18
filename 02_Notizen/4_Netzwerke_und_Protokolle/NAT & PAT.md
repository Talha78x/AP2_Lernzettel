# NAT & PAT

## Definition
**NAT (Network Address Translation)** übersetzt IP-Adressen zwischen einem internen und einem externen Netz. Meist werden dabei **private IPv4-Adressen** aus dem LAN in **öffentliche IPv4-Adressen** für das Internet umgesetzt.

**PAT (Port Address Translation)** erweitert dieses Prinzip, indem zusätzlich **Ports** umgeschrieben werden. Dadurch können viele interne Geräte gleichzeitig eine einzige öffentliche IPv4-Adresse nutzen.

## Warum ist das so?
Private IPv4-Adressen sind im Internet nicht routbar. Gleichzeitig sind öffentliche IPv4-Adressen knapp. NAT und PAT lösen deshalb zwei praktische Probleme:
- interne Netze können mit privaten Adressen arbeiten
- mehrere interne Geräte kommen trotzdem ins Internet

Darum ist NAT/PAT vor allem im IPv4-Alltag sehr verbreitet.

## Zusammenspiel
- [[IPv4 (Grundlagen & Subnetting usw..)]] liefert die privaten und öffentlichen Adressbereiche.
- [[Standardprotokolle (TCP, UDP, MAC, ARP, ICMP, HTTP, HTTPS, FTP, SMTP...)]] zeigt, warum bei PAT die Ports wichtig sind.
- [[OSI und TCP-IP Modell]] ordnet NAT/PAT logisch rund um Schicht 3/4 ein.
- [[VPN (Tunneling, standortübergreifende Kommunikation)]] kann NAT beeinflussen, weil Tunnel und Adressübersetzung zusammenspielen müssen.
- [[Firewall (IDS, IPS, DMZ, ACL, Filtertabelle)]] sitzt in der Praxis oft auf demselben Gateway wie NAT/PAT.

## Eigene Worte (prüfungsnah)
NAT ist ein Adress-Übersetzer am Netzrand. PAT ist die Variante, bei der nicht nur die Adresse, sondern zusätzlich die Portnummer hilft, viele interne Verbindungen auseinanderzuhalten.

## Arten von NAT
| Art | Beschreibung | Typischer Einsatz |
|---|---|---|
| Static NAT | feste 1:1-Zuordnung zwischen privater und öffentlicher IP | interner Server soll von außen erreichbar sein |
| Dynamic NAT | Zuordnung aus einem Pool öffentlicher Adressen | seltener im Alltag |
| PAT / NAT Overload | viele private IPs teilen sich eine öffentliche IP über Ports | Standard bei Internetzugang kleiner und mittlerer Netze |

## NAT und PAT im Vergleich
| Merkmal | NAT | PAT |
|---|---|---|
| Übersetzt IP-Adressen | ja | ja |
| Übersetzt Ports | nein oder nicht zwingend | ja |
| Viele interne Hosts über eine öffentliche IP | nur eingeschränkt | ja |
| Typische Verwendung | 1:1 oder Pool-Zuordnung | Internetzugang für viele Clients |

## Beispielhafter Ablauf bei PAT
### Ausgangslage
- PC1: `192.168.10.10`
- PC2: `192.168.10.11`
- Router außen: `203.0.113.5`

### Verbindungen
| Intern | Ziel | Übersetzung außen |
|---|---|---|
| `192.168.10.10:51500` | `93.184.216.34:443` | `203.0.113.5:40001` |
| `192.168.10.11:51501` | `93.184.216.34:443` | `203.0.113.5:40002` |

So kann der Router Antworten später wieder dem richtigen internen Gerät zuordnen.

## Vorteile und Grenzen
### Vorteile
- spart öffentliche IPv4-Adressen
- trennt interne und externe Adressräume
- interne Adressen sind von außen nicht direkt sichtbar

### Grenzen
- NAT ist **keine vollwertige Sicherheitsmaßnahme**
- eingehende Verbindungen brauchen oft Portweiterleitung
- manche Protokolle oder VPN-Verfahren reagieren empfindlich auf NAT

## Beispielaufgabe mit Lösung
**Aufgabe:** Warum können in einem Heimnetz viele Geräte gleichzeitig mit einer einzigen öffentlichen IPv4-Adresse ins Internet, obwohl jedes Gerät eine eigene private Adresse hat?

**Lösung:**
Weil der Router **PAT** verwendet.

**Begründung:**
1. Jedes interne Gerät sendet mit privater IP und eigenem Quellport.
2. Der Router ersetzt die private Quell-IP durch seine öffentliche IP.
3. Zusätzlich vergibt oder verwaltet er unterschiedliche externe Ports.
4. Antworten werden anhand dieser Portzuordnung dem richtigen internen Gerät zurückgegeben.

## Typische Prüfungsszenarien
- NAT und PAT unterscheiden.
- private und öffentliche IPv4-Adressen korrekt einordnen.
- erklären, warum NAT bei IPv4 wichtig und bei IPv6 weniger zentral ist.
- Portweiterleitung und Erreichbarkeit interner Server beschreiben.

## Merksätze
- NAT übersetzt Adressen.
- PAT übersetzt Adressen plus Ports.
- Viele Clients, eine öffentliche IP: Das ist der klassische PAT-Fall.
- NAT erhöht Struktur, ersetzt aber keine Firewall.
