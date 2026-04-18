# Archivierung (Archivbit)

## Definition
**Archivierung** ist die langfristige, geordnete und oft revisionssichere Aufbewahrung von Daten, meist aus rechtlichen, organisatorischen oder historischen Gründen. Sie ist **nicht** dasselbe wie ein Backup.

Das **Archivbit** ist ein älteres Dateiattribut, das anzeigt, ob eine Datei seit der letzten Sicherung verändert wurde. Es spielt vor allem im klassischen Backup-Kontext eine Rolle, nicht als Kernprinzip moderner Archivierung.

## Warum ist das so?
Unternehmen müssen Daten aus unterschiedlichen Gründen aufbewahren:
- zur Wiederherstellung nach Fehlern oder Ausfällen
- zur Erfüllung gesetzlicher Aufbewahrungspflichten
- zur Nachvollziehbarkeit von Geschäftsvorgängen

Diese Ziele sind unterschiedlich. Deshalb muss man zwischen **Datensicherung** und **Archivierung** sauber trennen.

## Zusammenspiel
- [[Backupstrategien (Vollbackup, inkrementell, differentiell, kontinuierlich)]] erklärt den Unterschied zur Sicherung.
- [[DSGVO und IT-Grundschutz (Personbezogene Daten usw..)]] beeinflusst, welche Daten wie lange aufbewahrt oder gelöscht werden dürfen.
- [[Band, Platte, NAS, SAN, Cloud, USB und optische Datenträger als Sicherungsmedien]] betrifft die Auswahl geeigneter Medien.
- [[Notfallkonzept, Disaster Recovery]] nutzt Backups, nicht primär Archive, zur schnellen Wiederherstellung.

## Eigene Worte (prüfungsnah)
Ein Backup ist für die Wiederherstellung nach einem Schaden gedacht. Ein Archiv ist für die langfristige, nachvollziehbare Aufbewahrung gedacht. Wer diese beiden Begriffe verwechselt, liegt in Prüfungen fast immer falsch.

## Backup vs. Archivierung
| Merkmal | Backup | Archivierung |
|---|---|---|
| Ziel | Wiederherstellung | langfristige Aufbewahrung |
| Änderung / Rotation | wird überschrieben oder rotiert | oft unveränderbar abgelegt |
| Zeitbezug | kurz- bis mittelfristig | langfristig |
| Fokus | Verfügbarkeit | Nachweis, Compliance, Historie |

## Typische Eigenschaften der Archivierung
| Merkmal | Bedeutung |
|---|---|
| revisionssicher | Daten dürfen nicht unbemerkt verändert werden |
| unveränderbar / WORM | einmal schreiben, vielfach lesen |
| nachvollziehbar | Zugriffe und Aufbewahrung sind dokumentiert |
| aufbewahrungspflichtig | abhängig von rechtlichen Vorgaben |

## Archivbit kurz erklärt
Das Archivbit zeigt klassisch an, ob eine Datei seit der letzten Sicherung verändert wurde.

Typische Logik:
- Datei geändert -> Archivbit gesetzt
- Voll- oder inkrementelles Backup -> Archivbit kann zurückgesetzt werden
- differentielles Backup -> Archivbit bleibt oft gesetzt

## Beispielaufgabe mit Lösung
**Aufgabe:** Ein Unternehmen muss Rechnungen zehn Jahre unveränderbar aufbewahren. Ist dafür primär ein Backup oder eine Archivierung vorgesehen?

**Lösung:**
**Archivierung**

**Begründung:**
Hier geht es nicht um schnelle Wiederherstellung nach Datenverlust, sondern um langfristige, manipulationssichere Aufbewahrung aus rechtlichen Gründen.

## Typische Prüfungsszenarien
- Backup und Archivierung unterscheiden.
- WORM-Prinzip erklären.
- Archivbit in klassischen Backupaufgaben einordnen.
- erklären, warum ein normales rollierendes Backup keine Archivierung ersetzt.

## Merksätze
- Backup rettet Betrieb, Archivierung erfüllt Aufbewahrungszwecke.
- Archivierung ist langfristig und oft unveränderbar.
- Das Archivbit gehört fachlich zu klassischen Sicherungsverfahren, nicht zum Kernzweck der Archivierung.
