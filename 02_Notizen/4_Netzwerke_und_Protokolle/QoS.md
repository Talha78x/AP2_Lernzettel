# QoS

**QoS (Quality of Service)** bezeichnet Mechanismen in einem Netzwerk, die bestimmte Datenpakete priorisieren, um die Kommunikationsqualität für zeitkritische Dienste sicherzustellen. 

Ohne QoS gilt im Netzwerk das *Best-Effort*-Prinzip: Alle Pakete werden gleich behandelt. Das führt bei einer stark ausgelasteten Verbindung (z. B. im WAN oder VPN-Tunnel) dazu, dass Pakete verzögert ankommen oder verloren gehen.

Besonders Dienste wie **VoIP-Telefonie** oder **Videokonferenzen** reagieren extrem empfindlich auf:
- **Latenz (Delay):** Die Verzögerung, bis das Paket ankommt.
- **Jitter:** Schwankungen in der Verzögerungszeit.
- **Paketverlust:** Wenn Router überlastet sind und Pakete verwerfen.

Mit QoS kann man am Switch oder Router einstellen, dass Sprachpakete absolute Vorfahrt vor beispielsweise einem normalen FTP-Download oder HTTP-Traffic bekommen. Die Bandbreite im Netzwerk wird durch QoS nicht erhöht, aber die vorhandene Bandbreite wird zugunsten wichtiger Echtzeitdienste sinnvoller verteilt.

Das Thema passt ideal zu [[Netzwerkkomponenten]], [[Standardprotokolle TCP, UDP, MAC, ARP, ICMP, HTTP, HTTPS, FTP, SMTP....]] (UDP ist bei VoIP besonders auf QoS angewiesen) und [[LAN, WAN, WLAN ....]].
