# Skript- und Shellprogrammierung

Skript- und Shellprogrammierung ist für Systemintegratoren (FISI) ein zentrales Werkzeug zur [[Automatisierung]] von administrativen Routineaufgaben. Im Gegensatz zu kompilierten Sprachen (wie C++) werden Skripte zur Laufzeit von einem Interpreter gelesen und ausgeführt.

Die beiden wichtigsten Werkzeuge für die Prüfung sind:
- **Bash (Linux):** Die Standard-Shell in unixoide Systemen. Typische Aufgaben sind das Automatisieren von Backups (siehe [[Backupstrategien Vollbackup, inkrementell, differentiell, kontinuierlich]]), das Setzen von Dateiberechtigungen (`chmod`, `chown`) oder das massenhafte Anlegen von Benutzern.
- **PowerShell (Windows):** Das moderne Automatisierungs-Framework von Microsoft. Es ist vollständig [[Programmierparadigmen prozedural, objektorientiert, funktional, deklarativ|objektorientiert]]. PowerShell nutzt sogenannte *Cmdlets* (wie `Get-Process` oder `New-ADUser`) zur Steuerung des Systems und von [[Active Directory und LDAP]].

In der Prüfung wird oft verlangt, kleine Skript-Abläufe (z.B. eine Schleife über eine CSV-Datei zum Anlegen von Usern) mittels [[Pseudocode]] darzustellen oder Grundlagenbefehle der Shell-Programmierung zu erkennen.

Querverweise: [[Automatisierung]], [[Betriebssysteme und Anwendungen]], [[Befehlezeilenkomandos ping, tracert, nslookup, ipconfig, ifconfig, netstat, nmap, tcpdump, dig ....]].
