# IPv6 Grundlagen Subnetting usw...

Weil die 32-Bit-Adressen von IPv4 erschöpft sind, nutzt **IPv6** 128 Bit lange Adressen. Diese werden hexadezimal in acht Blöcken zu je 16 Bit geschrieben (z.B. `2001:0db8:85a3::8a2e:0370:7334`).

Eine klassische Subnetzmaske in Dezimalschreibweise gibt es bei IPv6 nicht mehr. Stattdessen wird ausschließlich die **Präfixlänge** (z. B. `/64`) genutzt, um Netz- und Hostanteil zu trennen.

**Wichtige Unterschiede zu IPv4:**
- Ein typisches IPv6-Subnetz hat **immer** ein `/64`-Präfix. Die hinteren 64 Bit bilden die Interface-ID (den Hostanteil).
- Es gibt **keine Broadcast-Adressen** mehr, diese Funktion übernehmen Multicast-Adressen.
- Es gibt **kein ARP** mehr, stattdessen wird das Neighbor Discovery Protocol (NDP) über ICMPv6 genutzt.

Beim **IPv6-Subnetting** geht es meistens darum, ein vom Provider zugewiesenes Präfix (oft `/48` oder `/56`) in mehrere `/64`-Netze aufzuteilen. Wenn man z.B. ein `/48`-Präfix hat, stehen 16 Bit für das Subnetting zur Verfügung, was sensationelle 65.536 mögliche Teilnetze ergibt.

Dieses Thema grenzt sich direkt von [[IPv4 Grundlagen Subnetting usw...]] ab und ist wichtig für moderne Netzwerke, [[Routing statisch, dynamisch, Inter-VLAN, Protokolle wie OSPF, RIP, BGP]] und [[Standardprotokolle TCP, UDP, MAC, ARP, ICMP, HTTP, HTTPS, FTP, SMTP....]].
