# SIEM usw..

**SIEM (Security Information and Event Management)** ist die Königsklasse der zentralen Log-Auswertung und ein wichtiges Thema in modernen Unternehmensnetzen.

Ein SIEM-System sammelt Log-Daten aus **allen** möglichen Quellen gleichzeitig: [[Event-Logs, Syslog|Syslog-Meldungen]], Windows Event-Logs, Firewall-Logs, IDS/IPS-Alarme, Authentifizierungslogs des [[Active Directory und LDAP|Active Directorys]] und Anwendungslogs. All diese Daten werden zentralisiert, korreliert und mit Echtzeit-Alarmen versehen.

**Was macht ein SIEM besonders?**
Die **Korrelation von Ereignissen**: Ein einzelnes fehlgeschlagenes Login ist uninteressant. Aber 5.000 fehlgeschlagene Logins in 60 Sekunden von derselben IP auf 50 verschiedene Konten ist ein eindeutiger Brute-Force-Angriff (siehe [[Angriffsarten und Schutzmanahmen]]). Das SIEM erkennt dieses Muster automatisch und schlägt Alarm.

Bekannte SIEM-Lösungen: Splunk, IBM QRadar, Microsoft Sentinel (Cloud-basiert).

Querverweise: [[Monitoring und SNMP]], [[Event-Logs, Syslog]], [[Angriffsarten und Schutzmanahmen]].
