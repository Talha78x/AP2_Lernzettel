# VLAN Arten, Trunking ....

Ein **VLAN** (*Virtual Local Area Network*) teilt ein physisches Netzwerk logisch in mehrere getrennte Broadcast-Domänen auf. Dadurch kann man Abteilungen, Rollen oder Sicherheitszonen sauber voneinander trennen, obwohl dieselbe Switch-Infrastruktur verwendet wird.

Wichtige Portarten sind:
- **Access-Port**: verbindet meist Endgeräte und transportiert normalerweise nur **ein** VLAN.
- **Trunk-Port**: transportiert **mehrere VLANs gleichzeitig** über eine physische Verbindung.

Beim **Trunking** werden Ethernet-Frames typischerweise nach **IEEE 802.1Q** mit einer VLAN-ID markiert. So kann ein Switch erkennen, zu welchem VLAN ein Frame gehört, obwohl viele VLANs dieselbe Leitung nutzen.

Wichtige Prüfungsmerksätze:
- Ein Trunk verbindet oft **Switches untereinander**, manchmal auch Switch und Router oder Switch und Server.
- Ein Access-Port ist typischerweise für **Clients, Drucker oder andere Endgeräte** gedacht.
- Über 802.1Q sind bis zu **4094 aktive VLAN-IDs** möglich.
- Zusätzlich gibt es oft eine **Native VLAN**-Konfiguration für ungetaggten Verkehr.

Das Thema passt besonders gut zu [[Netzwerkkomponenten]], [[Routing statisch, dynamisch, Inter-VLAN, Protokolle wie OSPF, RIP, BGP]], [[First-Hop Redundancy Protocol FHRP]] und [[Spanning Tree]].
