# Routing (statisch, dynamisch, Inter-VLAN, Protokolle wie OSPF, RIP, BGP)

Routing ist der Prozess, mit dem Router entscheiden, über welchen Weg ein Datenpaket von Quelle zu Ziel transportiert wird.

**Statisches Routing:**
Ein Administrator trägt die Routen manuell in die Routing-Tabelle ein. Ändert sich die Netzwerktopologie (z.B. ein Link fällt aus), muss der Admin manuell eingreifen. Geeignet für kleine, stabile Netze.

**Dynamisches Routing:**
Router tauschen automatisch Informationen aus und berechnen selbstständig die besten Wege. Fällt ein Link aus, findet das Protokoll automatisch einen Alternativpfad.
- **RIP (Routing Information Protocol):** Sehr altes Distance-Vector-Protokoll. Zählt Hops (Router-Sprünge) als Metrik. Maximal 15 Hops. Heute kaum noch im Einsatz.
- **OSPF (Open Shortest Path First):** Link-State-Protokoll. Jeder Router kennt die gesamte Netztopologie (eine "Karte"). Berechnet den schnellsten Weg via Dijkstra-Algorithmus. Standard in Enterprise-Netzen.
- **BGP (Border Gateway Protocol):** Das Routing-Protokoll des Internets. Wird zwischen autonomen Systemen (AS) eingesetzt, also zwischen großen Netzwerken wie Internetprovidern (ISPs).

**Inter-VLAN Routing:**
Ohne Routing können Geräte in verschiedenen [[VLAN Arten, Trunking ....|VLANs]] nicht miteinander kommunizieren. Inter-VLAN-Routing kann über einen dedizierten Router (Router-on-a-Stick via Trunk-Link) oder direkt über einen Layer-3-Switch realisiert werden.

Querverweise: [[Netzwerkkomponenten]], [[VLAN Arten, Trunking ...]].
