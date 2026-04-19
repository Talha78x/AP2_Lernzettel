# Troubleshooting und Härtungsmaßnahmen

## Definition
**Troubleshooting** ist die systematische Fehleranalyse und -behebung.  
**Härtung** (Hardening) reduziert Angriffsflächen durch sichere Konfigurationen.

## Warum ist das so?
Fehlerbehebung allein reicht nicht: Ohne Härtung kommen Störungen oder Angriffe häufig zurück.

## Zusammenspiel
- Startpunkt meist Alarm aus [[Monitoring und SNMP]] oder Incident im [[Ticketsysteme]].
- Analyse entlang OSI-Schichten (Physik → Anwendung).
- Nach Behebung: Hardening, Dokumentation in [[SOP]], Lessons Learned.

## Troubleshooting-Methodik
| Schritt | Inhalt |
|---|---|
| Eingrenzen | Wer ist betroffen? Seit wann? |
| Hypothese | Plausible Ursache formulieren |
| Test | Messung/Log-Prüfung/Change-Rollback |
| Fix | Kleinster wirksamer Eingriff |
| Verifikation | Funktion + Nebenwirkungen prüfen |

## Härtungsmaßnahmen (Beispiele)
- Unnötige Dienste deaktivieren
- Patchstand aktuell halten
- MFA/Passwortrichtlinien erzwingen
- Least-Privilege/Rollenkonzepte
- Logging und SIEM-Anbindung

## Beispielaufgabe
**Aufgabe:** Webdienst antwortet langsam. CPU normal, aber DB-Latenz hoch. Was tun?  
**Lösung:** Ursache in DB-Pfad prüfen (Index, Locking, IO), nicht blind Webserver skalieren.

## Eigene Worte
Gutes Troubleshooting arbeitet datenbasiert statt nach Bauchgefühl. Hardening macht aus einer „reparierten“ eine „robuste“ Umgebung.

## Typische Prüfungsszenarien
- OSI-orientierte Fehlersuche
- Quick Fix vs. nachhaltige Maßnahme
- Dokumentationspflicht nach Incident

## Querverweise
[[SOP]] · [[SIEM usw..|SIEM usw...]] · [[SLA]]
