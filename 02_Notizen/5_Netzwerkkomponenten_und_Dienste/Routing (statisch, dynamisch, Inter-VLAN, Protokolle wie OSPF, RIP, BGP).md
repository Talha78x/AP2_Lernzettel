# Routing (statisch, dynamisch, Inter-VLAN, Protokolle wie OSPF, RIP, BGP)

## Definition
**Routing** ist der Prozess, mit dem ein Router oder Layer-3-System entscheidet, über welchen Weg ein Datenpaket zu einem Zielnetz gesendet wird. Grundlage dafür ist die **Routing-Tabelle**.

## Warum ist das so?
Ein einzelnes LAN reicht in der Praxis selten aus. Unternehmen haben:
- mehrere Subnetze
- verschiedene VLANs
- Internetanbindung
- Außenstellen oder Provider-Verbindungen

Damit Pakete das richtige Zielnetz erreichen, müssen Wege bekannt und auswählbar sein.

## Zusammenspiel
- [[IPv4 (Grundlagen & Subnetting usw..)]] und [[IPv6 (Grundlagen & Subnetting usw..)]] liefern Netzpräfixe.
- [[VLAN (Arten, Trunking ...)]] braucht Routing für Kommunikation zwischen VLANs.
- [[Netzwerkkomponenten]] ordnet Router und Layer-3-Switches ein.
- [[First-Hop Redundancy Protocol (FHRP)]] ergänzt Routing um Gateway-Redundanz.
- [[NAT & PAT]] sitzt oft auf dem Edge-Router.

## Eigene Worte (prüfungsnah)
Routing heißt: Ein Gerät entscheidet nicht nur "senden oder nicht", sondern konkret "über welchen nächsten Weg komme ich ins richtige Netz?". Geroutet wird immer netzbezogen, nicht hostbezogen im Layer-2-Sinn.

## Statisches und dynamisches Routing
| Art | Funktionsweise | Vorteil | Nachteil |
|---|---|---|---|
| statisch | Routen manuell eintragen | einfach, kontrollierbar | unflexibel bei Änderungen |
| dynamisch | Router tauschen Wege automatisch aus | anpassungsfähig | komplexer |

## Dynamische Routing-Protokolle
| Protokoll | Typ | Merkmal | Prüfungsrelevanz |
|---|---|---|---|
| RIP | Distance Vector | zählt Hops, max. 15 | historisch wichtig |
| OSPF | Link State | berechnet beste Wege mit Topologiewissen | Standard in Enterprise-Netzen |
| BGP | Path Vector / Exterior | Routing zwischen autonomen Systemen | Internet-Routing |

## RIP, OSPF, BGP grob erklärt
### RIP
- einfaches älteres Routing-Protokoll
- Metrik = Anzahl der Hops
- für moderne große Netze ungeeignet

### OSPF
- Router kennen die Topologie ihres Bereichs
- berechnen den besten Pfad
- schnell und leistungsfähig in Unternehmensnetzen

### BGP
- verbindet große eigenständige Netze
- wichtig zwischen Providern und autonomen Systemen
- weniger "kürzester Weg", mehr policy-orientierte Pfadwahl

## Inter-VLAN-Routing
Geräte in unterschiedlichen VLANs können ohne Routing nicht direkt miteinander sprechen.

Typische Lösungen:
| Lösung | Beschreibung |
|---|---|
| Router-on-a-Stick | ein Router mit Trunk-Link und Subinterfaces |
| Layer-3-Switch | Routing direkt im Switch |

## Standardroute
Wenn kein speziellerer Eintrag vorhanden ist, wird oft die **Default Route** genutzt. Sie zeigt typischerweise Richtung Internet oder Upstream-Router.

## Beispielaufgabe mit Lösung
**Aufgabe:** Ein PC in VLAN 10 soll einen Server in VLAN 20 erreichen. Beide VLANs liegen auf demselben Switch, aber die Kommunikation funktioniert nicht. Warum?

**Lösung:**
Wahrscheinlich fehlt **Inter-VLAN-Routing**.

**Begründung:**
1. VLANs sind getrennte logische Netze.
2. Ein normaler Layer-2-Switch trennt diese Broadcast-Domänen.
3. Erst ein Router oder Layer-3-Switch verbindet die Netze über Routing.

## Typische Prüfungsszenarien
- statisches und dynamisches Routing vergleichen.
- RIP, OSPF und BGP grob einordnen.
- Default Route erklären.
- begründen, warum VLAN-Kommunikation Routing benötigt.
- Router-on-a-Stick beschreiben.

## Merksätze
- Geroutet wird zwischen Netzen, nicht nur zwischen Geräten.
- VLAN-Trennung macht Inter-VLAN-Routing nötig.
- RIP ist einfach, OSPF ist Enterprise, BGP ist Internet.
