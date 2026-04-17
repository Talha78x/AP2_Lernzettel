# Netzwerkkomponenten

Netzwerkkomponenten sind die physischen (oder virtuellen) Bausteine eines jeden IT-Netzwerks. In der IHK-Prüfung muss man die Unterschiede exakt benennen können.

- **Hub (veraltet):** Dummes Gerät auf Layer 1. Leitet jedes empfangene Paket an **alle** anderen Ports weiter. Erzeugt massive Kollisionen. Heute vollständig durch Switches ersetzt.
- **Switch (Layer 2):** Lernt MAC-Adressen und leitet Pakete intelligent nur an den richtigen Zielport weiter (MAC-Adress-Tabelle). Layer-3-Switches können zusätzlich routen (Inter-VLAN Routing). Bildet das Rückgrat des LANs.
- **Router (Layer 3):** Verbindet verschiedene Netzwerke (z.B. LAN mit WAN/Internet) und entscheidet anhand von IP-Adressen und Routing-Tabellen, welchen Weg ein Paket nehmen soll.
- **Access Point (AP):** Bietet die WLAN-Anbindung für Endgeräte. Er stellt eine Brücke zwischen dem kabelgebundenen Netz und dem Funk-Medium dar.
- **Proxy:** Ein Vermittler zwischen Client und Internet. Kann Webseiten cachen (Performance), bestimmte Seiten sperren (Filter) und die IP-Adresse des Clients verstecken (Anonymisierung).
- **VPN-Konzentrator / Gateway:** Nimmt verschlüsselte VPN-Verbindungen von externen Clients entgegen und terminiert sie ins interne Netz.

Querverweise: [[Firewall (IDS, IPS, DMZ, ACL, Filtertabelle)]], [[Routing (statisch, dynamisch, Inter-VLAN, Protokolle wie OSPF, RIP, BGP)]], [[VLAN Arten, Trunking ...]].
**