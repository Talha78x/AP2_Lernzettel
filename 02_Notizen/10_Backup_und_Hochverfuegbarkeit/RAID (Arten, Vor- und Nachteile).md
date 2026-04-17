# RAID Arten, Vor- und Nachteile

Ein **RAID** (Redundant Array of Independent Disks) bündelt mehrere physische Festplatten zu einem logischen Laufwerk. Ziel ist eine höhere Ausfallsicherheit (Redundanz) und/oder ein höherer Datendurchsatz. **Wichtig:** Ein RAID ersetzt niemals ein [[Backupstrategien Vollbackup, inkrementell, differentiell, kontinuierlich|Backup]]!

**RAID 0 (Striping):**
- *Funktion:* Daten werden in Blöcke aufgeteilt und abwechselnd auf mindestens 2 Platten geschrieben.
- *Vorteile:* Maximale Lese- und Schreibgeschwindigkeit, 100 % der Kapazität nutzbar.
- *Nachteile:* **Keine Redundanz.** Fällt eine Platte aus, sind *alle* Daten zerstört.

**RAID 1 (Mirroring / Spiegelung):**
- *Funktion:* Daten werden auf mindestens 2 Platten exakt gespiegelt geschrieben.
- *Vorteile:* Hohe Ausfallsicherheit. Fällt eine Platte aus, läuft das System normal weiter. Schnelles Lesen.
- *Nachteile:* Nur 50 % der Gesamtkapazität nutzbar (teuer pro GB).

**RAID 5:**
- *Funktion:* Benötigt mindestens 3 Platten. Daten und Paritätsinformationen (zur Fehlerkorrektur) werden rotierend über alle Platten verteilt.
- *Vorteile:* Guter Kompromiss aus Sicherheit, Geschwindigkeit und nutzbarem Platz. Es darf genau 1 Platte ausfallen. Nutzbare Kapazität: $(n-1) \cdot \text{Kapazität der kleinsten Platte}$.
- *Nachteile:* Beim Ausfall einer Platte bricht die Performance massiv ein. Das Wiederherstellen (Rebuild) nach einem Plattenwechsel dauert sehr lange.

**RAID 6:**
- *Funktion:* Wie RAID 5, aber mit doppelter, verteilter Parität. Benötigt mindestens 4 Platten.
- *Vorteile:* Es dürfen **zwei** Platten gleichzeitig ausfallen. Nutzbare Kapazität: $(n-2)$.
- *Nachteile:* Schreibvorgänge sind durch die doppelte Paritätsberechnung langsamer.

**RAID 10 (1+0):**
- *Funktion:* Ein RAID 0, das auf mehreren RAID 1-Verbünden aufbaut. Benötigt mindestens 4 Platten.
- *Vorteile:* Kombiniert die extreme Geschwindigkeit von RAID 0 mit der hohen Ausfallsicherheit von RAID 1. Ideal für Datenbanken.
- *Nachteile:* Sehr teuer, da nur 50 % der Kapazität nutzbar sind.

Querverweise: [[Server und Storage]], [[Band, Platte, NAS, SAN, Cloud, USB und optische Datentrager als Sicherungsmedien]].
