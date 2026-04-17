# Betriebssysteme und Anwendungen

Das **Betriebssystem (OS)** bildet die Schnittstelle zwischen der Hardware eines Computers und der darauf laufenden Anwendungssoftware. Es verwaltet Ressourcen (CPU, Speicher, I/O-Geräte) und stellt grundlegende Dienste zur Verfügung.

**Klassifikation von Betriebssystemen:**
- **Multi-User (Mehrbenutzersystem):** Mehrere Benutzer können gleichzeitig auf dem System arbeiten (z. B. Windows Server über Remote Desktop, Linux-Terminal-Server).
- **Multitasking:** Das OS kann scheinbar mehrere Aufgaben gleichzeitig ausführen, indem der Scheduler (Prozessverwaltung) die CPU-Zeit rasant zwischen den Programmen wechselt. Bei *präemptivem Multitasking* behält das OS die volle Kontrolle und kann Prozessen die CPU-Zeit entziehen.
- **Echtzeitsystem (Real-Time OS):** Garantiert die Verarbeitung von Ereignissen innerhalb einer fest definierten, harten Zeitspanne. Extrem wichtig bei [[Cyber-physische Systeme Sensoren, Aktoren und Bibliotheken|Industrieanlagen]] oder in der Medizintechnik.

Anwendungen setzen auf dem OS auf. In großen Infrastrukturen werden Anwendungen heute selten manuell installiert, sondern über Skripte (siehe [[Skript- und Shellprogrammierung]]) oder [[Deploymentstrategien]] automatisiert verteilt.

Querverweise: [[Virtualisierung Bare-Metal, Hypervisor, Container]], [[2-Tier-, 3-Tier- und Multi-Tier-Architekturen]].
