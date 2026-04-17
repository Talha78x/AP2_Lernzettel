# Archivierung

In der IHK-Prüfung muss man den Unterschied zwischen **Backup (Datensicherung)** und **Archivierung** glasklar benennen können. Beide Konzepte erfüllen völlig unterschiedliche Zwecke.

**Backup (Datensicherung):**
- *Zweck:* Kurz- und mittelfristige Wiederherstellung von Daten nach einem Ausfall, einem Systemfehler oder einem versehentlichen Löschen (siehe [[Notfallkonzept, Disaster Recovery]]).
- *Eigenschaft:* Backups werden ständig überschrieben oder rolliert (siehe Generationenprinzip unter [[Backupstrategien Vollbackup, inkrementell, differentiell, kontinuierlich]]). Sie sind dynamisch.

**Archivierung:**
- *Zweck:* Langfristige, revisionssichere und unveränderbare Aufbewahrung von Daten aus gesetzlichen oder historischen Gründen.
- *Gesetzliche Vorgaben:* In Deutschland fordern u.a. das HGB (Handelsgesetzbuch) und die GoBD (Grundsätze zur ordnungsmäßigen Führung und Aufbewahrung von Büchern), dass z.B. Rechnungen, Jahresabschlüsse und geschäftliche E-Mails 6 bis 10 Jahre **manipulationssicher** aufbewahrt werden.
- *Eigenschaft:* Einmal ins Archiv geschriebene Daten dürfen (bis zum Ablauf der Frist) nicht mehr verändert oder gelöscht werden (WORM-Prinzip: Write Once, Read Many). 
- *Medium:* Werden Dateien archiviert, werden sie oft vom schnellen Primär-Storage gelöscht, um Platz zu schaffen, und auf langsame, günstige Medien (z.B. [[Band, Platte, NAS, SAN, Cloud, USB und optische Datentrager als Sicherungsmedien|Tapes]]) verschoben.

Querverweise: [[DSGVO und IT-Grundschutz Personbezogene Daten usw...]], [[Backupstrategien Vollbackup, inkrementell, differentiell, kontinuierlich]].
