# Berechnung von Backup- und Wiederherstellungsdauer, Bandbreite, Speicherbedarf inkl. Komprimierung.

Berechnungsaufgaben zu Backups sind ein absoluter Dauerbrenner in der FISI-Abschlussprüfung (Teil 2). Hierbei muss man extrem auf die Einheiten (Bit vs. Byte, Faktor 1000 vs. 1024) achten.

**1. Einheiten umrechnen:**
- Speichergrößen werden in der Regel mit dem Faktor 1024 gerechnet (eigentlich Gibibyte = GiB), in alten IHK-Aufgaben manchmal auch mit 1000. Achte auf den Text! (1 TB = 1024 GB = 1.048.576 MB).
- Netzwerkkapazitäten (Bandbreite) werden in **Bit pro Sekunde** angegeben (z.B. 1 Gbit/s = 1.000 Mbit/s = 1.000.000 kbit/s). 
- *Wichtig:* Um von Gbit/s (Netzwerk) auf MByte/s (Speicher) zu kommen, muss man durch 8 teilen!
  *(Beispiel: Eine 1 Gbit/s-Leitung überträgt im Idealfall 125 MByte pro Sekunde).*

**2. Berechnung der Übertragungsdauer:**
- Formel: $\text{Zeit (in Sekunden)} = \frac{\text{Datenmenge (in MByte)}}{\text{Übertragungsrate (in MByte/s)}}$
- *Overhead:* Bei Netzwerkübertragungen fordert die IHK oft, einen Protokoll-Overhead (z.B. 20% für TCP/IP-Header) abzuziehen. Dann ist die *effektive* Nutzdatenrate nur 80% der theoretischen Bandbreite.

**3. Speicherbedarf mit Komprimierung:**
- Wenn ein Vollbackup von 5 TB mit einer Komprimierungsrate von 2:1 durchgeführt wird, halbiert sich die zu speichernde Datenmenge auf 2,5 TB.
- *Tipp:* Wenn in der Aufgabe steht "Die Komprimierung spart 30% ein", dann rechnest du $\text{Datenmenge} \times 0,7$.

**4. Differentielles vs. Inkrementelles Wachstum:**
- Oft muss der Speicherbedarf für 2 Wochen berechnet werden:
  - Bei Inkrementell: $1 \times \text{Vollbackup} + 13 \times \text{tägliche Änderung}$.
  - Bei Differentiell: $1 \times \text{Vollbackup} + (\text{Tag 1} + \text{Tag 2} + ... + \text{Tag 13})$, da die differentielle Datei jeden Tag größer wird.

Querverweise: [[Backupstrategien Vollbackup, inkrementell, differentiell, kontinuierlich]], [[Anforderungen an Bandbreite, Latenz, Verfugbarkeit, Ubertragungsmedien und Netzwerksicherheit]].
