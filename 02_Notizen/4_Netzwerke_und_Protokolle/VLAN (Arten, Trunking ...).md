# VLAN (Arten, Trunking ...)

## Definition
Ein **VLAN (Virtual Local Area Network)** trennt ein physisches Netzwerk logisch in mehrere **Broadcast-Domänen**. Geräte können dadurch trotz gemeinsamer Switch-Infrastruktur in getrennten logischen Netzen arbeiten.

## Warum ist das so?
Ohne VLANs wären alle Geräte an einem Switch oft in derselben Broadcast-Domäne. Das führt zu Nachteilen:
- mehr Broadcast-Verkehr
- schwächere Trennung zwischen Abteilungen oder Sicherheitszonen
- unflexible Netzstruktur

VLANs schaffen Ordnung, Sicherheit und bessere Skalierbarkeit, ohne dass für jede Gruppe ein eigener physischer Switch nötig ist.

## Zusammenspiel
- [[OSI und TCP-IP Modell]] ordnet VLANs vor allem auf Schicht 2 ein.
- [[IPv4 (Grundlagen & Subnetting usw..)]] und [[IPv6 (Grundlagen & Subnetting usw..)]] liefern die Subnetze, die oft je VLAN getrennt werden.
- [[Routing (statisch, dynamisch, Inter-VLAN, Protokolle wie OSPF, RIP, BGP)]] verbindet VLANs über Inter-VLAN-Routing.
- [[Spanning Tree]] schützt geschaltete Netze vor Schleifen.
- [[First-Hop Redundancy Protocol (FHRP)]] sichert das Default Gateway pro VLAN ab.

## Eigene Worte (prüfungsnah)
Ein VLAN ist wie eine unsichtbare Trennwand im Switch. Zwei PCs können am selben Gerät angeschlossen sein und trotzdem logisch in unterschiedlichen Netzen arbeiten, als wären sie an getrennten Switches.

## Grundbegriffe
| Begriff | Bedeutung |
|---|---|
| VLAN-ID | Kennnummer des VLANs |
| Broadcast-Domäne | Bereich, in dem Broadcasts verteilt werden |
| Access-Port | Port für genau ein VLAN, meist für Endgeräte |
| Trunk-Port | Port für mehrere VLANs gleichzeitig |
| 802.1Q | Standard zum Tagging von VLAN-Frames |

## Access-Port und Trunk-Port
| Porttyp | Aufgabe | Typisches Ziel |
|---|---|---|
| Access | genau ein VLAN | PC, Drucker, IP-Telefon |
| Trunk | mehrere VLANs über eine Leitung | Switch zu Switch, Switch zu Router, Switch zu Hypervisor |

## Trunking mit 802.1Q
Bei **802.1Q** erhält ein Ethernet-Frame einen VLAN-Tag. Dadurch erkennt das empfangende Gerät, zu welchem VLAN ein Frame gehört.

**Wichtig:**
- Access-Ports senden Frames meist ungetaggt.
- Trunks transportieren mehrere VLANs parallel.
- Das **Native VLAN** ist meist das VLAN für ungetaggte Frames auf einem Trunk.

## Typische VLAN-Arten
| Art | Bedeutung |
|---|---|
| Daten-VLAN | normales Benutzer- oder Abteilungsnetz |
| Management-VLAN | Verwaltung von Switches und Infrastruktur |
| Voice-VLAN | getrennte Priorisierung und Struktur für VoIP |
| Native VLAN | ungetaggter Verkehr auf dem Trunk |

## Warum VLAN allein nicht reicht
VLANs trennen logisch, aber Kommunikation **zwischen** VLANs ist ohne Routing nicht möglich.

Beispiel:
- VLAN 10 = Vertrieb
- VLAN 20 = Buchhaltung

Wenn ein PC aus VLAN 10 einen Server in VLAN 20 erreichen soll, braucht man **Inter-VLAN-Routing** über Router oder Layer-3-Switch.

## Beispielaufgabe mit Lösung
**Aufgabe:** Ein Switch hat Port 1 für einen PC aus VLAN 10 und Port 24 als Verbindung zu einem zweiten Switch. Über Port 24 sollen VLAN 10, VLAN 20 und VLAN 30 übertragen werden. Welcher Porttyp ist passend?

**Lösung:**
- Port 1: **Access-Port**, weil der PC nur in einem VLAN arbeitet.
- Port 24: **Trunk-Port**, weil mehrere VLANs über dieselbe Verbindung laufen sollen.

**Begründung:**
Ein Access-Port gehört normalerweise zu genau einem VLAN, ein Trunk transportiert mehrere VLANs per 802.1Q-Tagging.

## Typische Prüfungsszenarien
- Access-Port und Trunk-Port unterscheiden.
- erklären, warum VLANs Broadcast-Domänen trennen.
- 802.1Q und VLAN-Tagging beschreiben.
- begründen, warum zwischen VLANs Routing nötig ist.

## Merksätze
- Ein VLAN ist eine logische Netztrennung auf gemeinsamer Hardware.
- Access = ein VLAN, Trunk = mehrere VLANs.
- VLAN-Trennung ersetzt kein Routing.
- Ein VLAN entspricht in der Praxis oft einem eigenen IP-Subnetz.
