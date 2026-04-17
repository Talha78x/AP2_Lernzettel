# Dateifreigaben und Datenabruf, z. B. SMB, CIFS und ODBC

Um im Netzwerk Dateien und Datenquellen bereitzustellen, nutzt man Dateifreigabe-Protokolle, die meist nach dem [[Client-Server und Peer-to-Peer|Client-Server-Prinzip]] funktionieren.

**SMB (Server Message Block) / CIFS (Common Internet File System):**
SMB ist das Standard-Netzwerkprotokoll von Windows für Dateifreigaben, Drucker und andere Schnittstellen. CIFS ist eine alte, von Microsoft abgewandelte Variante von SMB (SMB 1.0), der Begriff wird heute aber oft noch synonym für SMB verwendet. Aktuelle Versionen (wie SMB 3.x) bieten starke Verschlüsselung und hohe Performance. Linux-Systeme nutzen das Softwarepaket *Samba*, um SMB-Freigaben bereitzustellen oder darauf zuzugreifen.

**ODBC (Open Database Connectivity):**
Im Gegensatz zu SMB, das ganze Dateien freigibt, ist ODBC eine standardisierte Datenbankschnittstelle. Sie ermöglicht es Anwendungen (Clients), unabhängig vom konkret eingesetzten Datenbankmanagementsystem (wie MySQL, MSSQL) auf die eigentlichen Datenbankinhalte des Servers zuzugreifen.

Für die Prüfung:
- **SMB/CIFS** = Datei- und Druckerfreigabe.
- **ODBC** = Schnittstelle für den Abruf von Datenbankinhalten.
- In Linux-lastigen Umgebungen ist die Alternative zu SMB oft das Network File System (NFS).

Das Thema verbindet sich gut mit [[Standardprotokolle TCP, UDP, MAC, ARP, ICMP, HTTP, HTTPS, FTP, SMTP....]], [[Relationale, nicht relationale NoSQL Datenbanken]] und [[SQL Befehle Aufbau, Arten und JOINs]].


oder 


# Dateifreigaben und Datenabruf, z. B. SMB, CIFS und ODBC

Damit Benutzer im Netzwerk auf zentrale Dateien zugreifen können, werden Dateifreigaben eingesetzt. Der Server stellt einen Ordner bereit, den Clients über das Netzwerk einbinden ("mappen").

**SMB / CIFS:**
- **SMB (Server Message Block):** Das Standardprotokoll für Dateifreigaben in Windows-Umgebungen. Ermöglicht Clients, auf Ordner und Drucker auf einem Windows-Server (oder Samba-Linux-Server) zuzugreifen.
- **CIFS:** Eine ältere Microsoft-Implementierung von SMB (eigentlich SMBv1). In modernen Umgebungen abgelöst durch SMBv2 und SMBv3, die deutlich sicherer und performanter sind. SMBv1 sollte zwingend deaktiviert werden (Einfallstor für WannaCry).
- *Ports:* TCP 445 (direkt) und 139 (über NetBIOS).

**ODBC (Open Database Connectivity):**
Eine standardisierte Schnittstelle, die es Anwendungen erlaubt, Daten aus verschiedenen Datenbanksystemen (z.B. MySQL, MSSQL, Oracle) abzurufen, ohne datenbankspezifischen Code schreiben zu müssen. Sehr relevant für Anwendungen, die auf Backend-Datenbanken zugreifen (siehe [[Relationale, nicht relationale NoSQL Datenbanken]] und [[APIs und REST]]).

Querverweise: [[Netzwerkkomponenten]], [[Active Directory und LDAP]].
