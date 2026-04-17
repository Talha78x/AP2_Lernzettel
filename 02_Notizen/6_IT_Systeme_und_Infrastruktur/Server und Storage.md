# Server und Storage

**Server** stellen im [[Client-Server und Peer-to-Peer|Client-Server-Modell]] Dienste und Ressourcen bereit. Moderne Server-Hardware zeichnet sich durch hohe Redundanz aus (z. B. doppelte Netzteile, ECC-RAM, mehrere Netzwerkkarten).

**Storage (Speicherarchitekturen):**
In Unternehmensnetzwerken reicht lokaler Speicher (DAS - Direct Attached Storage) oft nicht aus. Stattdessen werden netzwerkbasierte Speicherlösungen eingesetzt:

1. **NAS (Network Attached Storage):**
   - Ein dedizierter Dateiserver, der Speicherplatz auf Dateiebene (File-Level) im Netzwerk bereitstellt.
   - Zugriff erfolgt meist über Protokolle wie [[Dateifreigaben und Datenabruf, z. B. SMB, CIFS und ODBC|SMB/CIFS oder NFS]].
   - Einfach einzurichten und gut für Dateifreigaben im Büro.

2. **SAN (Storage Area Network):**
   - Ein hochperformantes, vom restlichen LAN getrenntes Netzwerk, das Speicher auf Blockebene (Block-Level) bereitstellt.
   - Der Server "denkt", die Festplatte sei lokal verbaut.
   - Zugriff erfolgt meist über Fibre Channel (FC) oder iSCSI.
   - Teuer, komplex, aber extrem schnell und unverzichtbar für große Datenbanken oder als Speicher-Backend für [[Virtualisierung Bare-Metal, Hypervisor, Container]].

Querverweise: [[RAID Arten, Vor- und Nachteile]], [[Band, Platte, NAS, SAN, Cloud, USB und optische Datentrager als Sicherungsmedien]].
