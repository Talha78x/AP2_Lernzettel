# Monitoring und SNMP

Monitoring (Systemüberwachung) ist für FISIs essenziell, um Ausfälle frühzeitig zu erkennen, bevor der Endbenutzer sie bemerkt. Ein konsistentes Monitoring-System überwacht Kriterien wie CPU-Auslastung, freien Speicherplatz, Netzwerkbandbreite und die Erreichbarkeit von Diensten (z.B. per [[Befehlezeilenkomandos ping, tracert, nslookup, ipconfig, ifconfig, netstat, nmap, tcpdump, dig ....|Ping oder Port-Check]]).

Der absolute De-facto-Standard zur Überwachung von Netzwerkgeräten (Router, Switches, Server) ist **SNMP (Simple Network Management Protocol)**.
- **Funktionsweise:** Eine zentrale Management-Station (der SNMP-Manager, z.B. PRTG, Nagios, Zabbix) fragt regelmäßig Daten von den SNMP-Agenten (den Endgeräten) ab. 
- **MIB (Management Information Base):** Eine hierarchische Datenbankstruktur auf dem Gerät, in der die abfragbaren Werte (die OIDs) definiert sind.
- **SNMP-Traps:** Im Gegensatz zur regelmäßigen Abfrage (Polling) durch den Manager, sendet das Endgerät bei einem kritischen Ereignis (z.B. einem Lüfterausfall) *aktiv* und unaufgefordert eine Alarmmeldung (Trap) an den Manager.

**SNMP-Versionen für die Prüfung:**
- *SNMPv1 & v2c:* Übertragen Daten und das Passwort (die "Community String", oft `public` oder `private`) völlig unverschlüsselt im Klartext. Ein großes Sicherheitsrisiko!
- *SNMPv3:* Der aktuelle Standard. Unterstützt starke Authentifizierung und [[Verschlusselung Arten, Symmetrisch, Asymmetrisch, Hybride|Verschlüsselung]] (authPriv) der übertragenen Monitoring-Daten.

Querverweise: [[Event-Logs, Syslog]], [[Ticketsysteme]].
