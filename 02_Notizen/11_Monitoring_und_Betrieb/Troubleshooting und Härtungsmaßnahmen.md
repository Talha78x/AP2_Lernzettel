# Troubleshooting und Hartungsmanahmen

**Troubleshooting (Fehlersuche):**
Wenn ein System streikt, müssen FISIs systematisch vorgehen, anstatt blind Einstellungen zu verändern. Ein bewährter Ansatz orientiert sich am [[OSI und TCP-IP Modell]]: Man prüft Fehler von unten nach oben.
1. Layer 1: Steckt das Kabel? Hat das Gerät Strom?
2. Layer 2: Leuchtet der Link am Switch? Sind die MAC-Adressen sichtbar? Stimmt das [[VLAN Arten, Trunking ....|VLAN]]?
3. Layer 3: Ist das Gerät per [[Befehlezeilenkomandos ping, tracert, nslookup, ipconfig, ifconfig, netstat, nmap, tcpdump, dig ....|Ping oder Tracert]] erreichbar? Stimmt das Routing?
4. Layer 4-7: Blockiert eine [[Firewall IDS, IPS, DMZ, ACL, Filtertabelle|Firewall]] den Port? Läuft der Webdienst? 
Dazu gehört auch das gründliche Lesen der [[Event-Logs, Syslog|Log-Dateien]].

**Härtungsmaßnahmen (System Hardening):**
Härtung bedeutet, ein System nach der Grundinstallation so abzusichern, dass die Angriffsfläche minimiert wird (siehe [[Angriffsarten und Schutzmanahmen]] und Security by Design). 
*Typische Maßnahmen für IHK-Prüfungen:*
- **Unnötige Dienste deaktivieren:** Was nicht läuft, kann nicht angegriffen werden.
- **Standard-Passwörter ändern:** Router oder Server niemals mit `admin/admin` betreiben.
- **Least Privilege:** Nur die absolut nötigen Berechtigungen vergeben (siehe [[Zutritts-, Zugangs- und Zugriffskontrolle]]).
- **Patch-Management:** Das Betriebssystem und alle Anwendungen stets auf dem neuesten Stand halten.

Querverweise: [[Monitoring und SNMP]], [[Befehlezeilenkomandos ping, tracert, nslookup, ipconfig, ifconfig, netstat, nmap, tcpdump, dig ....]].
