# Netzwerkkomponenten

## Definition
**Netzwerkkomponenten** sind Geräte oder virtuelle Funktionen, die Netzwerkkommunikation ermöglichen, steuern, absichern oder erweitern. Sie arbeiten auf unterschiedlichen Schichten und haben klar verschiedene Aufgaben.

## Warum ist das so?
Ein Netzwerk besteht nicht nur aus Kabeln und PCs. Für Kommunikation werden unterschiedliche Funktionen benötigt:
- Signale weiterleiten
- lokale Ziele finden
- Netze verbinden
- Funkzugänge bereitstellen
- Verkehr filtern oder umleiten

Darum gibt es verschiedene Komponenten mit jeweils eigener Rolle.

## Zusammenspiel
- [[OSI und TCP-IP Modell]] hilft bei der Schichteinordnung.
- [[Routing (statisch, dynamisch, Inter-VLAN, Protokolle wie OSPF, RIP, BGP)]] baut auf Routern oder Layer-3-Switches auf.
- [[Firewall (IDS, IPS, DMZ, ACL, Filtertabelle)]] ergänzt Schutzfunktionen.
- [[VLAN (Arten, Trunking ...)]] und [[Spanning Tree]] betreffen vor allem Switch-Infrastrukturen.
- [[LAN, WAN, WLAN ....]] zeigt die Umgebungen, in denen diese Komponenten eingesetzt werden.

## Eigene Worte (prüfungsnah)
Netzwerkkomponenten sind die Werkzeuge des Netzes. Ein Switch verbindet Geräte innerhalb eines LANs intelligent, ein Router verbindet unterschiedliche Netze, ein Access Point bringt Clients ins WLAN und eine Firewall kontrolliert, was passieren darf.

## Wichtige Komponenten im Überblick
| Komponente | Schicht / Schwerpunkt | Aufgabe |
|---|---|---|
| Hub | Layer 1 | sendet Signale an alle Ports weiter |
| Switch | Layer 2 | leitet Frames anhand von MAC-Adressen gezielt weiter |
| Layer-3-Switch | Layer 2/3 | Switching plus Routing, oft Inter-VLAN |
| Router | Layer 3 | verbindet unterschiedliche Netze |
| Access Point | LAN/WLAN-Brücke | stellt Funkzugang bereit |
| Firewall | Sicherheitskontrolle | filtert und überwacht Verkehr |
| Proxy | Vermittlungsinstanz | vermittelt Anfragen, kann filtern/cachen |
| VPN-Gateway | Tunnel-Endpunkt | terminiert sichere VPN-Verbindungen |

## Hub, Switch und Router im Vergleich
| Gerät | Kennt MAC? | Kennt IP? | Typische Aufgabe |
|---|---|---|---|
| Hub | nein | nein | reine Signalverteilung |
| Switch | ja | meist nein | Kommunikation im selben LAN |
| Router | nicht als Kernfunktion | ja | Kommunikation zwischen Netzen |

## Access Point
Ein **Access Point** verbindet drahtlose Clients mit dem kabelgebundenen Netz. Er ist kein "WLAN-Router" im engeren Sinn, sondern oft Teil einer größeren Netzwerkinfrastruktur.

## Proxy
Ein **Proxy** sitzt logisch zwischen Client und Zielsystem.

Typische Aufgaben:
- Caching
- Inhaltsfilter
- Zugriffskontrolle
- Protokollierung
- Verbergen interner Client-Anfragen

## Beispielaufgabe mit Lösung
**Aufgabe:** Ein Gerät soll zwei unterschiedliche IP-Netze miteinander verbinden. Ist dafür eher ein Switch oder ein Router zuständig?

**Lösung:**
Ein **Router**.

**Begründung:**
Ein Router arbeitet mit IP-Netzen und Routing-Entscheidungen. Ein reiner Layer-2-Switch verbindet dagegen hauptsächlich Teilnehmer innerhalb desselben logischen Netzes.

## Typische Prüfungsszenarien
- Hub, Switch und Router unterscheiden.
- Access Point richtig einordnen.
- Layer-3-Switch von Router abgrenzen.
- erklären, welche Komponente zwischen zwei Netzen routet.
- Proxy und Firewall nicht verwechseln.

## Merksätze
- Hub sendet an alle, Switch gezielt, Router netzübergreifend.
- Ein Switch verbindet meist Teilnehmer, ein Router verbindet Netze.
- Ein Access Point ist die Funkbrücke ins LAN.
