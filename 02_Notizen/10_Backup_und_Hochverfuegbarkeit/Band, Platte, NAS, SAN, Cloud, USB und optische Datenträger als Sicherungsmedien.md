# Band, Platte, NAS, SAN, Cloud, USB und optische Datenträger als Sicherungsmedien

## Definition
**Sicherungsmedien** sind die Speicherorte oder Speichertechnologien, auf denen Backups oder archivierte Daten abgelegt werden. Die Wahl des Mediums beeinflusst Kosten, Geschwindigkeit, Ausfallsicherheit und Schutz vor Angriffen.

## Warum ist das so?
Nicht jedes Medium passt zu jedem Sicherungsziel. Wichtige Fragen sind:
- Wie groß ist die Datenmenge?
- Wie schnell muss gesichert oder wiederhergestellt werden?
- Wie lange sollen Daten aufbewahrt werden?
- Soll das Medium online, offline oder extern gelagert werden?

Darum muss das Sicherungsmedium zum Schutzbedarf und zur Backupstrategie passen.

## Zusammenspiel
- [[Backupstrategien (Vollbackup, inkrementell, differentiell, kontinuierlich)]] bestimmt, wie oft und in welchem Umfang gesichert wird.
- [[Archivierung (Archivbit)]] ist bei Langzeitaufbewahrung relevant.
- [[Berechnung von Backup- und Wiederherstellungsdauer anhand von Bandbreite, Geschwindigkeit, Datenmenge und Komprimierung]] hilft bei der Größen- und Zeitplanung.
- [[Notfallkonzept, Disaster Recovery]] bewertet die Medien nach RTO und RPO.
- [[RAID (Arten, Vor- und Nachteile)]] ist Produktivspeicher-Redundanz, aber kein Ersatz für echte Sicherungsmedien.

## Eigene Worte (prüfungsnah)
Ein Sicherungsmedium ist nicht einfach nur "Speicherplatz". Es entscheidet mit darüber, wie schnell ein Restore möglich ist, wie gut ein Backup gegen Ransomware geschützt ist und wie wirtschaftlich die Lösung für große Datenmengen bleibt.

## Medien im Überblick
| Medium | Vorteil | Nachteil | Typischer Einsatz |
|---|---|---|---|
| Band / Tape | günstig pro TB, offline lagerbar | langsamer Zugriff, lineares Medium | Langzeitbackup, Offsite |
| Platte / Disk | schnell, einfacher Restore | online oft stärker gefährdet | Disk-to-Disk-Backup |
| NAS | einfach, netzbasiert | bei ständiger Erreichbarkeit angreifbar | Backup-Ziel im LAN |
| SAN | sehr performant | teuer und komplex | eher Primärspeicher, Spezialfälle |
| Cloud | extern, skalierbar | Internetabhängigkeit, laufende Kosten | Offsite-Backup |
| USB | günstig für kleine Umgebungen | manuell, fehleranfällig | kleine Büros |
| optische Datenträger | unveränderbar möglich | geringe Kapazität, unpraktisch | heute selten |

## Online, offline, offsite
| Begriff | Bedeutung |
|---|---|
| online | direkt im Netz erreichbar |
| offline | vom Netz getrennt |
| offsite | an anderem Ort gelagert |

Gerade offline oder offsite ist wichtig gegen Brand, Diebstahl oder Ransomware.

## Typische Auswahlkriterien
| Kriterium | Bedeutung |
|---|---|
| Datenmenge | beeinflusst Wirtschaftlichkeit |
| Restore-Geschwindigkeit | wichtig für RTO |
| Medienkosten | wichtig für Budget |
| Auslagerung | wichtig für Katastrophenschutz |
| Sicherheit / Unveränderbarkeit | wichtig gegen Manipulation und Malware |

## Beispielaufgabe mit Lösung
**Aufgabe:** Ein Unternehmen möchte große Sicherungen kostengünstig langfristig aufbewahren und vor Ransomware schützen. Welches Medium ist besonders passend?

**Lösung:**
**Band / Tape**

**Begründung:**
1. sehr günstige Kosten pro Terabyte
2. gut für Langzeitaufbewahrung
3. offline lagerbar und damit besser gegen Online-Angriffe geschützt

## Typische Prüfungsszenarien
- Tape, Disk und Cloud vergleichen.
- online/offline/offsite unterscheiden.
- NAS und SAN im Backup-Kontext einordnen.
- erklären, warum ein ständig eingebundenes Backupziel problematisch sein kann.

## Merksätze
- Schnelles Backupmedium ist nicht automatisch das sicherste.
- Offline schützt gut gegen viele Malware-Szenarien.
- Sicherungsmedium und Backupstrategie müssen zusammen gedacht werden.
