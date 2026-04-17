# IPv4 Grundlagen Subnetting usw...

**IPv4-Adressen** bestehen aus 32 Bit, die zur besseren Lesbarkeit in vier Dezimalblöcke (Oktette) unterteilt werden. Jede IPv4-Adresse ist durch eine **Subnetzmaske** (oder das CIDR-Präfix, z. B. `/24`) logisch in zwei Teile getrennt:
1. **Netzwerkanteil**: Identifiziert das konkrete Subnetz.
2. **Hostanteil**: Identifiziert das spezifische Gerät innerhalb dieses Subnetzes.

Beim **Subnetting** werden Bits vom Hostanteil "ausgeliehen" und dem Netzwerkanteil zugeschlagen. Dadurch entstehen aus einem großen Netzwerk mehrere kleinere Teilnetze. Das verbessert die Sicherheit, verringert Broadcast-Traffic und hilft, IP-Adressen sparsam zu nutzen.

**Wichtige Berechnungsregeln für Prüfungen:**
- **Netzwerkadresse**: Alle Host-Bits sind auf `0` gesetzt. Sie ist die erste IP im Subnetz und kann nicht an Geräte vergeben werden.
- **Broadcastadresse**: Alle Host-Bits sind auf `1` gesetzt. Sie ist die letzte IP im Subnetz und dient als Rundrufadresse.
- **Anzahl der Hosts**: Berechnet sich mit $2^n - 2$ (wobei $n$ die Anzahl der Host-Bits ist). Die `- 2` steht für die abgezogene Netzwerk- und Broadcastadresse.

Das Thema ist ein absolutes Kernthema und bildet die Basis für [[Routing statisch, dynamisch, Inter-VLAN, Protokolle wie OSPF, RIP, BGP]], [[NAT PAT]] und [[Standardprotokolle TCP, UDP, MAC, ARP, ICMP, HTTP, HTTPS, FTP, SMTP....]].
