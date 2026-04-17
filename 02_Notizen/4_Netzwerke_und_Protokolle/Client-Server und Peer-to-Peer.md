# Client-Server und Peer-to-Peer

In der Netzwerkarchitektur unterscheidet man grundlegend zwei Kommunikationsmodelle.

**Client-Server-Architektur:**
Das Netz ist streng hierarchisch aufgebaut. Ein zentraler **Server** stellt Ressourcen, Dienste oder Daten bereit. Die **Clients** greifen auf diese Dienste zu. 
- *Vorteile:* Zentrale Verwaltung, einfachere Datensicherung, hohe Sicherheit, gute Skalierbarkeit.
- *Nachteile:* Fällt der Server aus (Single Point of Failure), steht der Dienst still. Serverhardware ist teuer.
Dieses Modell ist der Standard in Unternehmensnetzwerken, z.B. bei einem [[Active Directory und LDAP]] oder bei der Bereitstellung von Webseiten über [[Standardprotokolle TCP, UDP, MAC, ARP, ICMP, HTTP, HTTPS, FTP, SMTP....|HTTP]].

**Peer-to-Peer-Architektur (P2P):**
Alle Rechner (Peers) im Netz sind gleichberechtigt. Jeder Knoten kann sowohl Dienste in Anspruch nehmen (als Client agieren) als auch eigene Ressourcen bereitstellen (als Server agieren).
- *Vorteile:* Keine teuren Server nötig, sehr ausfallsicher, da kein zentraler Single Point of Failure existiert.
- *Nachteile:* Schwer zu verwalten, Datensicherung ist dezentral extrem aufwendig, Sicherheit ist schwer durchzusetzen.

In modernen IT-Systemen wird P2P oft in Blockchain-Technologien oder Dezentralisierungskonzepten genutzt, während klassische Infrastruktur fast ausschließlich Client-Server ist. 
Verwandte Konzepte: [[Dateifreigaben und Datenabruf, z. B. SMB, CIFS und ODBC]], [[Betriebssysteme und Anwendungen]].
