# Notfallkonzept, Disaster Recovery

## Definition
Ein **Notfallkonzept** beschreibt, wie ein Unternehmen bei schweren Störungen oder Katastrophen handlungsfähig bleibt. **Disaster Recovery** konzentriert sich besonders auf die Wiederherstellung der IT nach einem Ausfall.

## Warum ist das so?
Schwere Vorfälle wie diese können den Betrieb massiv stören:
- Feuer
- Hochwasser
- Stromausfall
- Ransomware
- Hardware- oder Standortausfall

Ohne vorbereitete Abläufe gehen wertvolle Zeit, Daten und Handlungsfähigkeit verloren.

## Zusammenspiel
- [[Backupstrategien (Vollbackup, inkrementell, differentiell, kontinuierlich)]] liefern Wiederherstellungsgrundlagen.
- [[Berechnung von Backup- und Wiederherstellungsdauer anhand von Bandbreite, Geschwindigkeit, Datenmenge und Komprimierung]] hilft bei der praktischen Umsetzbarkeit.
- [[USV (Arten, Vor- und Nachteile)]] unterstützt Verfügbarkeit bei Stromproblemen.
- [[Schutzbedafsanalyse und Riskoanalyse]] und Business-Impact-Betrachtungen helfen bei der Priorisierung.

## Eigene Worte (prüfungsnah)
Ein Notfallkonzept sagt nicht nur, **dass** ein Backup existiert, sondern wie ein Unternehmen im Krisenfall konkret reagiert: Wer macht was, in welcher Reihenfolge und wie schnell müssen Systeme oder Daten wieder da sein?

## Wichtige Kennzahlen
| Kennzahl | Frage |
|---|---|
| RPO (Recovery Point Objective) | Wie viel Datenverlust ist maximal tolerierbar? |
| RTO (Recovery Time Objective) | Wie lange darf der Ausfall dauern? |

## RPO und RTO unterscheiden
| Begriff | Bedeutung | Beispiel |
|---|---|---|
| RPO | maximal tolerierter Datenverlust in der Zeit | 4 Stunden |
| RTO | maximal tolerierte Wiederanlaufzeit | 8 Stunden |

**Merke:** RPO = Daten, RTO = Zeit.

## Typische Bausteine eines Notfallkonzepts
| Baustein | Zweck |
|---|---|
| Priorisierung kritischer Systeme | was muss zuerst wiederhergestellt werden |
| Rollen und Zuständigkeiten | wer entscheidet und handelt |
| Kommunikationswege | wen informiert man wie |
| Wiederanlaufpläne | Reihenfolge der IT-Wiederherstellung |
| Tests / Übungen | Wirksamkeit prüfen |

## Warum Tests wichtig sind
Ein Notfallkonzept ist nur dann belastbar, wenn es regelmäßig geprüft wird:
- Restore-Test
- Tabletop-Übung
- Umschalt- oder Failover-Test

## Beispielaufgabe mit Lösung
**Aufgabe:** Ein Unternehmen akzeptiert maximal 2 Stunden Datenverlust, aber ein System darf höchstens 6 Stunden ausfallen. Wie lauten RPO und RTO?

**Lösung:**
- **RPO = 2 Stunden**
- **RTO = 6 Stunden**

**Begründung:**
RPO bezieht sich auf den tolerierbaren Datenverlust, RTO auf die maximal tolerierte Ausfallzeit.

## Typische Prüfungsszenarien
- RPO und RTO unterscheiden.
- Notfallkonzept von Backup-Konzept abgrenzen.
- Priorisierung kritischer Systeme erklären.
- begründen, warum Restore-Tests nötig sind.

## Merksätze
- Ein Backup allein ist noch kein Notfallkonzept.
- RPO misst Datenverlust, RTO misst Wiederherstellungszeit.
- Ungestestete Notfallpläne sind im Ernstfall riskant.
