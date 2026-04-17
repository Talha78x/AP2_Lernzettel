# Notfallkonzept, Disaster Recovery

Ein Notfallkonzept (oder Business Continuity Plan) regelt, wie ein Unternehmen bei schwerwiegenden IT-Ausfällen (z. B. durch Feuer, Hochwasser, Sabotage oder Ransomware) den Geschäftsbetrieb aufrechterhält oder schnellstmöglich wiederherstellt (Disaster Recovery).

Grundlage für das Konzept ist eine **Business Impact Analyse (BIA)**, in der ermittelt wird, wie kritisch bestimmte Geschäftsprozesse sind. Aus der BIA ergeben sich zwei absolute Kern-Kennzahlen für die IHK-Prüfung:

**1. RPO (Recovery Point Objective):**
- Beantwortet die Frage: *Wie viel Datenverlust ist maximal tolerierbar?*
- Es definiert den Zeitraum zwischen dem letzten erfolgreichen [[Backupstrategien Vollbackup, inkrementell, differentiell, kontinuierlich|Backup]] und dem Eintreten des Notfalls.
- *Beispiel:* Ein RPO von 4 Stunden bedeutet, dass das Backup höchstens 4 Stunden alt sein darf. Die Daten der letzten 3 Stunden und 59 Minuten dürfen notfalls verloren gehen.

**2. RTO (Recovery Time Objective):**
- Beantwortet die Frage: *Wie lange darf der Ausfall dauern?*
- Es definiert die Zeitspanne vom Eintritt des Notfalls bis zu dem Moment, in dem die IT-Systeme wieder produktiv zur Verfügung stehen müssen.
- *Beispiel:* Ein RTO von 8 Stunden bedeutet, dass nach dem Crash die Hardware beschafft, installiert, das Backup eingespielt und das System nach spätestens 8 Stunden wieder online sein muss.

Ein Notfallkonzept ist nur dann etwas wert, wenn es in der Praxis (z. B. durch Tabletop-Übungen oder reale Restore-Tests) regelmäßig getestet wird.

Querverweise: [[Schutzbedafsanalyse und Riskoanalyse]], [[USV Arten, Vor- und Nachteile]], [[Backupstrategien Vollbackup, inkrementell, differentiell, kontinuierlich]].
