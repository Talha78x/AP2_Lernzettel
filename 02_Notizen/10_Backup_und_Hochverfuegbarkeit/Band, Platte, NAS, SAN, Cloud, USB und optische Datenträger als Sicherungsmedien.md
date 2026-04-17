# Band, Platte, NAS, SAN, Cloud, USB und optische Datentrager als Sicherungsmedien

Für ein professionelles Backup-Konzept (siehe [[Backupstrategien Vollbackup, inkrementell, differentiell, kontinuierlich]]) reicht es nicht, Daten nur auf eine andere Partition zu kopieren. Die Wahl des Sicherungsmediums hängt von Datenmenge, Budget und Sicherheitsanforderungen (wie dem [[Notfallkonzept, Disaster Recovery|RTO und RPO]]) ab.

**1. Bandlaufwerke (Tapes, z.B. LTO):**
Der absolute Klassiker in Rechenzentren für Langzeitbackups.
- *Vorteile:* Enorme Speicherkapazität pro Band, extrem günstig pro Terabyte, ideal für Offline-Sicherungen (Schutz vor Ransomware, da Tapes im Safe liegen).
- *Nachteile:* Lineares Speichermedium (es muss gespult werden), langes Suchen nach einzelnen Dateien, teure Laufwerke.

**2. NAS (Network Attached Storage) & SAN (Storage Area Network):**
- *NAS:* Sehr beliebt für das Erst-Backup (Disk-to-Disk). Schnell, einfach erreichbar über SMB/NFS. Nachteil: Ist das NAS ständig im Netz gemountet, kann Ransomware auch das Backup verschlüsseln.
- *SAN:* Hochperformantes Block-Storage (Fibre Channel / iSCSI), oft für Enterprise-Virtualisierungsumgebungen genutzt, seltener als reines Backup-Ziel, eher als primärer Datenspeicher.

**3. Cloud-Backup:**
- *Vorteile:* Daten liegen physisch getrennt in einem Rechenzentrum (Brand-/Wasserschutz), flexibel skalierbar.
- *Nachteile:* Abhängigkeit von der Internet-[[Anforderungen an Bandbreite, Latenz, Verfugbarkeit, Ubertragungsmedien und Netzwerksicherheit|Bandbreite]] (ein 10-TB-Restore dauert über das Internet sehr lange), laufende Kosten, strikte [[DSGVO und IT-Grundschutz Personbezogene Daten usw...|Datenschutzvorgaben]] müssen beachtet werden (Auftragsverarbeitungsvertrag).

**4. USB-Festplatten (HDD/SSD) & Optische Datenträger (DVD/Blu-ray):**
- USB-Platten eignen sich für kleine Büros, erfordern aber oft manuelle Wechsel durch Mitarbeiter. Optische Datenträger sind heute aufgrund zu geringer Kapazitäten (maximal ca. 100 GB bei BDXL) für Firmenbackups praktisch ausgestorben.

Querverweise: [[Archivierung]], [[RAID Arten, Vor- und Nachteile]].
