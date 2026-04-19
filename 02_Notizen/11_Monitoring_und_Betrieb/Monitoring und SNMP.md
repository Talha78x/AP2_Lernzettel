# Monitoring und SNMP

## Definition
**Monitoring** überwacht kontinuierlich Verfügbarkeit, Performance und Fehlerzustände von IT-Systemen.  
**SNMP** ist ein Protokoll, mit dem Netzwerkgeräte Managementdaten bereitstellen.

## Warum ist das so?
Messwerte sind Voraussetzung für stabile Services, Kapazitätsplanung und SLA-Nachweise.

## Zusammenspiel
1. Geräte liefern Metriken per SNMP, API, Agent oder Logs.
2. Monitoring bewertet Schwellwerte und Trends.
3. Bei Verstößen: Alarm → [[Ticketsysteme]] → Supportprozess.
4. Sicherheitsereignisse können an [[SIEM usw..|SIEM usw...]] weitergegeben werden.

## SNMP in der Prüfung
| Begriff | Kurz erklärt | Wichtig |
|---|---|---|
| OID | eindeutiger Messpunkt | Prüfungsbegriff |
| MIB | Struktur der OIDs | Datenmodell |
| Polling | aktive Abfrage durch Manager | zyklisch |
| Trap/Inform | aktiver Event vom Gerät | schnellere Alarmierung |
| SNMPv3 | Auth + Verschlüsselung | Standard im Betrieb |

## Beispielaufgabe
**Aufgabe:** Pollingintervall 60 Sekunden, Link fällt um 09:10:20 aus. Wann spätestens erkannt?  
**Lösung:** Beim nächsten Poll spätestens um **09:11:00** (ohne Trap).

## Eigene Worte
Monitoring ist die „Vitalüberwachung“ der IT. SNMP ist dabei ein wichtiger Sensor, aber nicht der einzige.

## Typische Prüfungsszenarien
- Polling vs. Trap
- SNMPv2c vs. v3
- Monitoringdaten für SLA interpretieren

## Querverweise
[[SLA]] · [[SMART]] · [[SIEM usw..|SIEM usw...]] · [[Troubleshooting und Härtungsmaßnahmen]]
