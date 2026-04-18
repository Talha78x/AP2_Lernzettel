# Monitoring und SNMP

## Definition
**Monitoring** ist die kontinuierliche Überwachung von IT-Systemen (Server, Netzwerk, Dienste, Anwendungen), um Störungen frühzeitig zu erkennen und messbar zu machen.  
**SNMP (Simple Network Management Protocol)** ist ein Standardprotokoll, mit dem Netzwerkgeräte Zustandsdaten bereitstellen.

## Warum ist das so?
IT-Betrieb ist ohne Messwerte blind: Ausfälle, Kapazitätsengpässe oder Sicherheitsprobleme werden sonst erst bemerkt, wenn Benutzer schon betroffen sind. Monitoring schafft:
- Frühwarnung statt Feuerwehrmodus
- objektive Kennzahlen für [[SLA]]
- Grundlage für [[Troubleshooting und Härtungsmaßnahmen]]
- Nachweise für Verfügbarkeit, z. B. gegenüber Kunden

## Wie funktioniert das im Zusammenspiel?
1. **Datenquellen**: Hosts, Switches, Firewalls, Datenbanken, Cloud-Dienste.
2. **Erfassung**: Agent-basiert (z. B. Node Exporter) oder agentlos (SNMP, WMI, API).
3. **Speicherung/Auswertung**: Time-Series-DB + Regeln/Schwellwerte.
4. **Alarmierung**: Mail, Teams, Pager, Ticket.
5. **Abarbeitung**: Übergabe an [[Ticketsysteme]], Eskalation an [[1st-Level, 2nd-Level, 3rd-Level-Support]].

## SNMP kompakt (prüfungsnah)
| Begriff | Bedeutung | Prüfungsrelevanz |
|---|---|---|
| Manager | Zentrales Monitoring-System | Fragt Werte ab (Polling) |
| Agent | Dienst auf Zielgerät | Liefert Messwerte |
| MIB/OID | Strukturierte Messpunkte | OID identifiziert jeden Wert |
| Trap/Inform | Gerät meldet aktiv Ereignis | Alarm ohne Polling-Zyklus |
| SNMPv2c | Community-String, keine echte Sicherheit | Nur in Altumgebungen |
| SNMPv3 | Authentifizierung + Verschlüsselung | In der Praxis Standard |

## Eigene Worte (Konzept erklärt)
Monitoring ist wie ein Cockpit: Temperatur, Drehzahl und Warnlampen machen den Zustand sichtbar. SNMP ist dabei nur **eine** Messmethode – moderne Umgebungen kombinieren SNMP, Logs, APIs und Metriken.

## Beispielaufgabe mit Lösung
**Aufgabe:** Ein Link fällt um 10:02 Uhr aus. Pollingintervall ist 5 Minuten. Wann erkennt der Manager den Ausfall spätestens ohne Trap?  
**Lösung:** Spätestens beim nächsten Polling um **10:05 Uhr**.  
**Zusatz:** Mit Trap kann der Alarm nahezu sofort kommen.

## Typische Prüfungsszenarien
- SNMPv2c vs. SNMPv3 begründen
- Polling und Trap unterscheiden
- Monitoring-Kette von Alarm bis Ticket erklären

## Querverweise
[[SIEM usw...]] · [[SMART]] · [[SLA]] · [[Troubleshooting und Härtungsmaßnahmen]]
