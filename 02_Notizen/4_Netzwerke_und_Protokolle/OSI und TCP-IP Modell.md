# OSI und TCP-IP Modell

Das [[OSI und TCP-IP Modell|OSI-Modell]] ist ein Referenzmodell mit **7 Schichten**, während das [[OSI und TCP-IP Modell|TCP/IP-Modell]] in der Praxis meist mit **4 Schichten** beschrieben wird. Das OSI-Modell hilft vor allem beim systematischen Verstehen und Einordnen von Netzwerkfunktionen, während das TCP/IP-Modell enger an real verwendeten Internetprotokollen orientiert ist.

Die Zuordnung lässt sich grob so merken:
- **OSI 1-2** entsprechen im TCP/IP-Modell dem **Netzwerkzugang**.
- **OSI 3** entspricht der **Internetschicht**.
- **OSI 4** entspricht der **Transportschicht**.
- **OSI 5-7** werden im TCP/IP-Modell zur **Anwendungsschicht** zusammengefasst.

Auf der **Internetschicht** arbeitet vor allem IP. IP sorgt dafür, dass Pakete über Netzgrenzen hinweg zum Ziel geroutet werden. Auf der **Transportschicht** arbeiten unter anderem [[Standardprotokolle TCP, UDP, MAC, ARP, ICMP, HTTP, HTTPS, FTP, SMTP....|TCP und UDP]], die die Ende-zu-Ende-Kommunikation zwischen Anwendungen regeln.

Für das Verständnis im Alltag helfen typische Beispiele:
- **Schicht 1-2 / Netzwerkzugang**: Ethernet, Switch, MAC-Adresse.
- **Schicht 3 / Internet**: IP, ICMP, Router.
- **Schicht 4 / Transport**: TCP, UDP, Ports.
- **Schicht 5-7 / Anwendung**: HTTP, HTTPS, DNS, SMTP, IMAP.

Das OSI-Modell ist stärker **protokollunabhängig**, während TCP/IP stärker an konkrete Protokolle gebunden ist. Genau deshalb wird in Prüfungen oft das OSI-Modell zum Erklären genutzt und das TCP/IP-Modell für Praxisbeispiele. Besonders wichtig sind die Verknüpfungen zu [[Standardprotokolle TCP, UDP, MAC, ARP, ICMP, HTTP, HTTPS, FTP, SMTP....]], [[NAT PAT]], [[TLS SSL]] und [[VPN Tunneling, standortubergreifende Kommunikation]].
