# SLA

## Definition
**SLA (Service Level Agreement)** ist die vertragliche Vereinbarung messbarer Serviceziele zwischen Anbieter und Kunde.

## Warum ist das so?
Nur gemessene und definierte Qualität ist steuerbar. SLAs klären Erwartungen und Konsequenzen.

## Zusammenspiel
- Messung durch [[Monitoring und SNMP]]
- Bearbeitung über [[Ticketsysteme]]
- Einhaltung durch Rollenmodell [[1st-Level, 2nd-Level, 3rd-Level-Support]]

## Typische SLA-Kennzahlen
| Kennzahl | Beispiel |
|---|---|
| Verfügbarkeit | 99,9 % pro Monat |
| Reaktionszeit | P1 innerhalb 15 Minuten |
| Wiederherstellungszeit (RTO) | Dienst in 4 Stunden wiederhergestellt |
| Lösungszeit | P3 innerhalb 2 Arbeitstage |

## Rechenbeispiel Verfügbarkeit
**Aufgabe:** 99,9 % Monatsverfügbarkeit bei 30 Tagen. Wie viel Ausfallzeit ist erlaubt?  
**Lösung:** 30 Tage = 43.200 Minuten. 0,1 % davon = **43,2 Minuten**.

## Eigene Worte
SLA ist das "Messprotokoll" eines Services: Was, wie schnell und in welcher Qualität geliefert werden muss.

## Prüfungsszenarien
- SLA vs. OLA vs. UC unterscheiden
- Verfügbarkeit berechnen
- Prioritäten und Reaktionszeiten zuordnen
