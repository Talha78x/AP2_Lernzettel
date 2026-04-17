# Backupstrategien Vollbackup, inkrementell, differentiell, kontinuierlich

Ein sicheres Backup ist die letzte Rettung bei einem Datenverlust (siehe [[Angriffsarten und Schutzmanahmen|Ransomware]]). In der IHK-Prüfung muss man die drei klassischen Backup-Arten zwingend unterscheiden können. Im Betriebssystem hilft dabei oft das sogenannte **Archivbit**, das anzeigt, ob eine Datei seit dem letzten Backup verändert wurde.

**1. Vollbackup (Vollsicherung):**
Alle ausgewählten Daten werden komplett gesichert. Das Archivbit wird danach zurückgesetzt (gelöscht).
- *Vorteil:* Sehr einfache und schnelle Wiederherstellung (Restore), man braucht nur dieses eine Backup.
- *Nachteil:* Dauert sehr lange und benötigt enorm viel Speicherplatz.

**2. Differentielles Backup:**
Es werden alle Daten gesichert, die sich **seit dem letzten Vollbackup** geändert haben. Das Archivbit wird *nicht* zurückgesetzt.
- *Speicherbedarf/Zeit:* Mittel (wächst mit jedem Tag nach dem Vollbackup an).
- *Wiederherstellung:* Mittel. Man benötigt genau zwei Sicherungen: das letzte Vollbackup und das *letzte* differentielle Backup.

**3. Inkrementelles Backup:**
Es werden nur die Daten gesichert, die sich **seit dem allerletzten Backup** (egal ob voll oder inkrementell) geändert haben. Das Archivbit wird *immer* zurückgesetzt.
- *Speicherbedarf/Zeit:* Sehr gering, das Backup geht extrem schnell.
- *Wiederherstellung:* Sehr aufwendig und fehleranfällig. Man benötigt das Vollbackup und **alle** darauf folgenden inkrementellen Backups in der richtigen Reihenfolge. Ist nur ein Inkrement aus der Kette defekt, sind alle späteren Inkremente wertlos.

**Generationenprinzip (Großvater-Vater-Sohn):**
Eine klassische Rotationsstrategie:
- *Sohn:* Tägliche Backups (meist inkrementell oder differentiell).
- *Vater:* Wöchentliches Vollbackup.
- *Großvater:* Monatliches Vollbackup (wird oft physisch an einem anderen Ort ausgelagert).

Querverweise: [[Band, Platte, NAS, SAN, Cloud, USB und optische Datentrager als Sicherungsmedien]], [[Notfallkonzept, Disaster Recovery]].
