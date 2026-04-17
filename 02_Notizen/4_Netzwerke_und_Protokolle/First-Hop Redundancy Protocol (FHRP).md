# First-Hop Redundancy Protocol FHRP

[[First-Hop Redundancy Protocol FHRP|FHRP]] ist eine Protokollfamilie zur **Absicherung des Default Gateways** in einem Subnetz. Das Ziel ist, dass der Ausfall eines einzelnen Routers nicht sofort das gesamte Teilnetz vom Routing abschneidet.

Das Grundprinzip:
- Mehrere Router bilden gemeinsam eine Gruppe.
- Die Gruppe verwendet eine **virtuelle IP-Adresse** und meist auch eine **virtuelle MAC-Adresse**.
- Die Clients tragen diese virtuelle IP als **Default Gateway** ein.
- Ein Router arbeitet aktiv, ein anderer steht als Reserve bereit.

Fällt der aktive Router aus, übernimmt ein anderer Router automatisch die Gateway-Funktion. Für die Endgeräte bleibt das weitgehend transparent, weil sie weiterhin dieselbe virtuelle Gateway-Adresse verwenden.

Bekannte Vertreter sind:
- **HSRP**
- **VRRP**
- **GLBP**

FHRP ist besonders wichtig in Netzen mit hoher Verfügbarkeit. Das Thema hängt eng mit [[VLAN Arten, Trunking ....]], [[Routing statisch, dynamisch, Inter-VLAN, Protokolle wie OSPF, RIP, BGP]] und [[Snap-Shot, Versionierung, Hochverfugbarkeit Clustering, Load Balancing, FHRP]] zusammen.
