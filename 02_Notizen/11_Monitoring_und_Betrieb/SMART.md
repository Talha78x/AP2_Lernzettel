# SMART

## Definition
**S.M.A.R.T. (Self-Monitoring, Analysis and Reporting Technology)** ist ein Diagnosesystem von HDD/SSD zur Früherkennung möglicher Laufwerksausfälle.

## Warum ist das so?
Datenträger fallen oft nicht ohne Vorzeichen aus. SMART-Werte helfen, Risiken rechtzeitig zu erkennen.

## Zusammenspiel
- SMART-Daten werden in [[Monitoring und SNMP]] eingebunden.
- Bei Grenzwertverletzungen entsteht ein Ticket in [[Ticketsysteme]].
- Präventive Maßnahmen werden per [[SOP]] durchgeführt (Austausch, Backup-Prüfung).

## Wichtige SMART-Indikatoren (typisch)
| Attribut | Aussage |
|---|---|
| Reallocated Sectors | Bereits ersetzte defekte Sektoren |
| Pending Sectors | Verdächtige, noch nicht remappte Sektoren |
| Uncorrectable Errors | nicht korrigierbare Lesefehler |
| Temperature | thermische Belastung |
| Power-On Hours | Betriebsstunden |

## Beispielaufgabe
**Aufgabe:** Reallocated Sectors steigen innerhalb 7 Tagen von 5 auf 120. Empfehlung?  
**Lösung:** Datenträger als kritisch einstufen, zeitnah ersetzen, konsistente Datensicherung und Restore-Test durchführen.

## Eigene Worte
SMART ist wie ein Verschleißindikator beim Auto: kein 100%-Orakel, aber ein wertvolles Warnsignal.

## Typische Prüfungsszenarien
- Warum SMART kein Backup ersetzt
- Präventive Wartung begründen
- Kritische Attribute nennen

## Querverweise
[[Backupstrategien (Vollbackup, inkrementell, differentiell, kontinuierlich)]] · [[Monitoring und SNMP]]
