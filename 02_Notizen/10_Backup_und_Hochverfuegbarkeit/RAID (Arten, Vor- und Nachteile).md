# RAID (Arten, Vor- und Nachteile)

## Definition
**RAID (Redundant Array of Independent Disks)** kombiniert mehrere physische Festplatten zu einem logischen Verbund. Ziel ist mehr Leistung, mehr Ausfallsicherheit oder eine Kombination daraus.

## Warum ist das so?
Einzelne Festplatten sind Ausfallpunkte. Außerdem kann je nach Anforderung wichtig sein:
- schnelleres Lesen/Schreiben
- höhere Verfügbarkeit
- bessere Nutzung mehrerer Datenträger

RAID löst diese Ziele technisch unterschiedlich, je nach Level.

## Zusammenspiel
- [[Server und Storage]] nutzt RAID oft auf Server- oder Storage-Systemen.
- [[Backupstrategien (Vollbackup, inkrementell, differentiell, kontinuierlich)]] bleibt trotzdem zwingend nötig.
- [[Band, Platte, NAS, SAN, Cloud, USB und optische Datenträger als Sicherungsmedien]] grenzt Produktivspeicher von Backupmedien ab.
- [[Notfallkonzept, Disaster Recovery]] berücksichtigt RAID als Verfügbarkeitsmaßnahme, nicht als vollständige Wiederherstellungslösung.

## Eigene Worte (prüfungsnah)
RAID schützt primär gegen den Ausfall einzelner Festplatten und kann Leistung verbessern. Es ersetzt aber **niemals** ein Backup, weil es nicht gegen versehentliches Löschen, Malware oder logische Fehler schützt.

## Wichtige RAID-Level
| RAID | Idee | Vorteil | Nachteil |
|---|---|---|---|
| RAID 0 | Striping | sehr schnell, volle Kapazität | keine Redundanz |
| RAID 1 | Spiegelung | hohe Ausfallsicherheit | nur 50 % nutzbar |
| RAID 5 | Striping + einfache Parität | guter Kompromiss | Rebuild kritisch, 1 Platte Ausfall |
| RAID 6 | Striping + doppelte Parität | 2 Platten dürfen ausfallen | langsamer, mehr Overhead |
| RAID 10 | Spiegelung + Striping | schnell und ausfallsicher | teuer, 50 % nutzbar |

## Kapazitätsformeln
| RAID | Nutzbare Kapazität |
|---|---|
| RAID 0 | `n x kleinste Platte` |
| RAID 1 | `1 x kleinste Platte` bei 2 Platten |
| RAID 5 | `(n - 1) x kleinste Platte` |
| RAID 6 | `(n - 2) x kleinste Platte` |
| RAID 10 | etwa `50 %` der Gesamtkapazität |

## Typische Einordnung
| Bedarf | passender RAID-Typ |
|---|---|
| maximale Geschwindigkeit ohne Redundanz | RAID 0 |
| einfache Spiegelung | RAID 1 |
| guter Kompromiss für Fileserver | RAID 5 |
| höhere Sicherheit bei vielen Platten | RAID 6 |
| Datenbank / hohe Leistung plus Redundanz | RAID 10 |

## Typische Prüfungsfalle
**RAID ist kein Backup.**

Warum nicht?
- versehentlich gelöschte Datei ist auf allen Platten gelöscht
- Ransomware verschlüsselt den gesamten Verbund
- logische Fehler replizieren sich sofort

## Beispielaufgabe mit Lösung
**Aufgabe:** Vier Festplatten mit je 2 TB werden in RAID 5 betrieben. Wie groß ist die nutzbare Kapazität?

**Lösung:**
`(4 - 1) x 2 TB = 6 TB`

**Begründung:**
Bei RAID 5 wird die Kapazität einer Platte für Paritätsinformationen benötigt.

## Typische Prüfungsszenarien
- RAID-Level unterscheiden.
- nutzbare Kapazität berechnen.
- RAID 5 und RAID 6 vergleichen.
- erklären, warum RAID kein Backup ersetzt.

## Merksätze
- RAID erhöht Verfügbarkeit, nicht automatisch Datensicherung.
- RAID 0 ist schnell, aber riskant.
- RAID 10 ist stark, aber teuer.
