# Backupstrategien (Vollbackup, inkrementell, differentiell, kontinuierlich)

## Definition
**Backupstrategien** beschreiben, wie Daten regelmäßig gesichert werden, damit sie nach Verlust, Beschädigung oder Verschlüsselung wiederhergestellt werden können.

Wichtige Strategien sind:
- **Vollbackup**
- **inkrementelles Backup**
- **differentielles Backup**
- **kontinuierliche Datensicherung**

## Warum ist das so?
Ein einziges Sicherungsverfahren erfüllt nie alle Ziele gleichzeitig. Man muss abwägen zwischen:
- Sicherungsdauer
- Speicherbedarf
- Wiederherstellungsaufwand
- Aktualität der Daten

Darum gibt es unterschiedliche Strategien mit verschiedenen Vor- und Nachteilen.

## Zusammenspiel
- [[Berechnung von Backup- und Wiederherstellungsdauer anhand von Bandbreite, Geschwindigkeit, Datenmenge und Komprimierung]] vertieft die Rechenwege.
- [[Notfallkonzept, Disaster Recovery]] nutzt Backups zur Einhaltung von RPO und RTO.
- [[Band, Platte, NAS, SAN, Cloud, USB und optische Datenträger als Sicherungsmedien]] betrifft die Wahl der Ziele.
- [[Archivierung (Archivbit)]] grenzt Backup von langfristiger Aufbewahrung ab.

## Eigene Worte (prüfungsnah)
Backupstrategie heißt: Ich entscheide nicht nur, **dass** ich sichere, sondern **wie** ich sichere. Dabei muss ich wissen, ob mir schnelles Backup, schnelle Wiederherstellung oder besonders wenig Speicherplatz wichtiger ist.

## Die wichtigsten Strategien
| Strategie | Was wird gesichert? | Vorteil | Nachteil |
|---|---|---|---|
| Vollbackup | alle ausgewählten Daten | Restore sehr einfach | braucht viel Zeit und Platz |
| inkrementell | Änderungen seit letztem Backup | schnell, wenig Speicher | Restore aufwendig |
| differentiell | Änderungen seit letztem Vollbackup | Restore einfacher als inkrementell | Backup wächst täglich an |
| kontinuierlich | Änderungen nahezu laufend | sehr aktueller Stand | technisch aufwendiger |

## Inkrementell vs. differentiell
| Frage | inkrementell | differentiell |
|---|---|---|
| Bezugspunkt | letztes Backup | letztes Vollbackup |
| Sicherungsmenge pro Tag | meist klein | wird mit der Zeit größer |
| Restore | Vollbackup + alle Inkremente | Vollbackup + letztes Differenzial |

## Wiederherstellung
| Strategie | Für Restore benötigt |
|---|---|
| Vollbackup | nur das letzte Vollbackup |
| inkrementell | letztes Vollbackup + alle Inkremente in richtiger Reihenfolge |
| differentiell | letztes Vollbackup + letztes differentielles Backup |

## Kontinuierliche Datensicherung
Dabei werden Änderungen sehr zeitnah oder laufend gesichert. Das verbessert das mögliche **RPO**, ist aber technisch und organisatorisch anspruchsvoller.

## Generationenprinzip
Ein klassisches Rotationsschema ist **Großvater-Vater-Sohn**:
- täglich
- wöchentlich
- monatlich

Dadurch stehen mehrere Stände über unterschiedliche Zeiträume zur Verfügung.

## Beispielaufgabe mit Lösung
**Aufgabe:** Ein Unternehmen möchte täglich möglichst schnell sichern, aber bei der Wiederherstellung nur das letzte Vollbackup und genau eine weitere Sicherung benötigen. Welche Strategie passt?

**Lösung:**
**Differentielles Backup**

**Begründung:**
1. Es sichert Änderungen seit dem letzten Vollbackup.
2. Für die Wiederherstellung reicht das letzte Vollbackup plus das letzte differentielle Backup.
3. Das ist einfacher als bei inkrementellen Ketten.

## Typische Prüfungsszenarien
- inkrementell und differentiell unterscheiden.
- Wiederherstellungsaufwand vergleichen.
- Archivbit in klassischen Aufgaben einordnen.
- passende Strategie für gegebene Anforderungen auswählen.

## Merksätze
- Vollbackup ist einfach beim Restore, teuer beim Sichern.
- Inkrementell spart Zeit und Platz, kostet beim Restore.
- Differentiell ist der Mittelweg.
