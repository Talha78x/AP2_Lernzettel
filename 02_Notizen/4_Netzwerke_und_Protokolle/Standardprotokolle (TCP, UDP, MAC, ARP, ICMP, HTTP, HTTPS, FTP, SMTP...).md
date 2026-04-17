# Standardprotokolle TCP, UDP, MAC, ARP, ICMP, HTTP, HTTPS, FTP, SMTP....

Netzwerkkommunikation funktioniert nur, wenn auf mehreren Ebenen feste Regeln gelten. Diese Regeln heißen [[Standardprotokolle TCP, UDP, MAC, ARP, ICMP, HTTP, HTTPS, FTP, SMTP....|Protokolle]] und lassen sich gut mit dem [[OSI und TCP-IP Modell]] einordnen.

Auf der lokalen Ebene spielt die **MAC-Adresse** eine wichtige Rolle. Sie identifiziert eine Netzwerkkarte innerhalb eines lokalen Netzes. Damit ein Gerät im LAN Daten korrekt zustellen kann, muss oft erst eine IPv4-Adresse in eine MAC-Adresse aufgelöst werden. Dafür wird [[Standardprotokolle TCP, UDP, MAC, ARP, ICMP, HTTP, HTTPS, FTP, SMTP....|ARP]] verwendet.

**ARP** arbeitet im lokalen Netzwerk und löst bekannte IPv4-Adressen in MAC-Adressen auf. Der typische Ablauf ist: Anfrage senden, Antwort erhalten, Eintrag im Cache speichern. Für IPv6 übernimmt diese Aufgabe nicht ARP, sondern das in [[IPv6 Grundlagen Subnetting usw...]] relevante Neighbor Discovery Protocol.

**ICMP** ist ein Protokoll für Informations- und Fehlermeldungen auf der Internetschicht. Bekannte Werkzeuge wie `ping` und `tracert` beziehungsweise `traceroute` nutzen ICMP, um Erreichbarkeit oder Wege durch das Netzwerk zu prüfen.

Bei der Transportkommunikation sind vor allem **TCP** und **UDP** wichtig. TCP ist verbindungsorientiert und zuverlässig, weil Verbindungen aufgebaut und Übertragungen kontrolliert werden. UDP ist verbindungslos und schneller, bietet aber keine eingebaute Fehlerkorrektur.

Wichtige Dienste und typische Ports sind:
- **HTTP**: Port 80, unverschlüsselte Webübertragung.
- **HTTPS**: Port 443, verschlüsselte Webübertragung mit [[TLS SSL]].
- **SSH**: Port 22, sicherer Fernzugriff.
- **SMTP**: Port 25, Versand von E-Mails.
- **POP3**: Port 110, Abruf und lokales Herunterladen von E-Mails.
- **IMAP**: Port 143, Zugriff auf E-Mails direkt auf dem Server.
- **DNS**: Port 53, Namensauflösung von Domainnamen in IP-Adressen.
- **FTP**: meist Port 21 für die Steuerung und Port 20 für Datenübertragung.

Für Prüfungen ist wichtig, die Protokolle nicht nur auswendig zu kennen, sondern sie auch der richtigen Ebene zuzuordnen. Gute Querverbindungen bestehen zu [[OSI und TCP-IP Modell]], [[NAT PAT]], [[TLS SSL]], [[IPv4 Grundlagen Subnetting usw...]] und [[IPv6 Grundlagen Subnetting usw...]].
