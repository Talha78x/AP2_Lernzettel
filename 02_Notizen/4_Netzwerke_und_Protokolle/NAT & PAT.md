# NAT PAT

[[NAT PAT|NAT]] steht für *Network Address Translation* und übersetzt **private IP-Adressen** in eine **öffentliche IP-Adresse**. Das ist wichtig, weil interne Geräte im LAN meist mit privaten Adressen arbeiten, im Internet aber öffentliche Adressen benötigt werden.

Der Hauptnutzen von NAT ist:
- Einsparung öffentlicher IPv4-Adressen.
- Abschirmung interner Adressen nach außen.
- Trennung zwischen internem und externem Netz.

[[NAT PAT|PAT]] steht für *Port Address Translation* und wird oft auch als **NAT Overload** bezeichnet. Dabei teilen sich mehrere interne Geräte **eine einzige öffentliche IP-Adresse**, und die Zuordnung wird über unterschiedliche Portnummern vorgenommen.

Einfach gemerkt:
- **NAT** übersetzt Adressen.
- **PAT** übersetzt Adressen **und** nutzt zusätzlich Ports zur Unterscheidung vieler Verbindungen.

In der Praxis arbeitet NAT oder PAT meist auf dem Router oder an der Netzgrenze. Dadurch passt das Thema sehr gut zu [[IPv4 Grundlagen Subnetting usw...]], [[Standardprotokolle TCP, UDP, MAC, ARP, ICMP, HTTP, HTTPS, FTP, SMTP....]] und [[VPN Tunneling, standortubergreifende Kommunikation]].

Für Prüfungen ist wichtig, dass NAT/PAT vor allem bei **IPv4** eine große Rolle spielt. Es löst nicht alle Sicherheitsprobleme, erhöht aber die Struktur und reduziert die direkte Sichtbarkeit interner Hosts aus dem Internet.
