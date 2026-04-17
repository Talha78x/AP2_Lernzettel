# Befehlezeilenkomandos ping, tracert, nslookup, ipconfig, ifconfig, netstat, nmap, tcpdump, dig ....

Für die Fehlersuche in Netzwerken (Troubleshooting) muss ein FISI Kommandozeilenwerkzeuge (CLI) beherrschen, die in Prüfungen oft zur Diagnose fiktiver Probleme abgefragt werden.

**Die wichtigsten Befehle:**
- **ping:** Prüft die grundsätzliche Erreichbarkeit eines Hosts auf Schicht 3 ([[OSI und TCP-IP Modell|OSI-Schicht 3]]) mittels [[Standardprotokolle TCP, UDP, MAC, ARP, ICMP, HTTP, HTTPS, FTP, SMTP....|ICMP Echo Requests]].
- **tracert (Windows) / traceroute (Linux):** Zeigt den genauen Weg (die "Hops" bzw. Router) an, den ein IP-Paket zum Ziel nimmt. Gut, um herauszufinden, *wo* eine Verbindung abbricht.
- **ipconfig (Windows) / ifconfig oder ip (Linux):** Zeigt die lokale IP-Konfiguration an (IP-Adresse, Subnetzmaske, Default Gateway). Mit `ipconfig /all` sieht man auch DNS und MAC-Adresse.
- **nslookup / dig:** Fragt DNS-Server ab, um Domainnamen in IP-Adressen aufzulösen (oder umgekehrt). `dig` liefert unter Linux detailliertere Antworten.
- **netstat:** Zeigt aktive TCP/UDP-Netzwerkverbindungen, offene Ports und Routingtabellen des lokalen Rechners an. Wichtig, um zu prüfen, ob ein Dienst lauscht.
- **nmap:** Ein mächtiger Port-Scanner, der Netzwerke nach aktiven Hosts und offenen Ports durchsucht. (Wichtig für [[Schutzbedafsanalyse und Riskoanalyse]]).
- **tcpdump / Wireshark:** Sniffer-Tools, die den gesamten Netzwerkverkehr (Pakete) mitschneiden und detailliert analysieren.

Querverweise: [[Standardprotokolle TCP, UDP, MAC, ARP, ICMP, HTTP, HTTPS, FTP, SMTP....]], [[Troubleshooting und Hartungsmanahmen]].
