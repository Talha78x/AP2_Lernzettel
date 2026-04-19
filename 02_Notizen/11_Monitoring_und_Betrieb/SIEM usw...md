# SIEM usw...

## Definition
**SIEM (Security Information and Event Management)** sammelt, korreliert und bewertet sicherheitsrelevante Logs aus vielen Quellen, um Angriffe früh zu erkennen.

## Warum ist das so?
Einzelne Logeinträge wirken harmlos. Erst durch Korrelation wird ein Angriffsmuster sichtbar (z. B. viele Fehlanmeldungen + verdächtige Admin-Aktion).

## Zusammenspiel
- Datenquellen: Firewall, AD, Endpoint, Cloud, IDS/IPS.
- Monitoring meldet technische Ausfälle, SIEM bewertet Sicherheitsrisiken.
- Bei Vorfall: Ticket + Eskalation + Maßnahmen aus [[Troubleshooting und Härtungsmaßnahmen]].

## SIEM-Bausteine
| Baustein | Funktion |
|---|---|
| Log-Ingestion | Einsammeln und Normalisieren |
| Korrelation | Regeln über mehrere Quellen |
| Alerting | Alarm nach Schweregrad |
| Dashboards | Lagebild/Trends |
| Forensik | Suche nach IOC/Timeline |

## Beispiel-Prüfungsfall
**Aufgabe:** Ein Benutzerkonto hat 200 fehlgeschlagene Logins aus mehreren Ländern und danach erfolgreichen Admin-Login. Wie bewerten?  
**Lösung:** Sehr hoher Verdacht auf Account-Kompromittierung → Incident eröffnen, Konto sperren, MFA-Status prüfen, Logins forensisch auswerten.

## Eigene Worte
SIEM ist kein „magisches Tool“, sondern ein Frühwarnsystem. Gute Regeln + gute Datenqualität entscheiden über Nutzen.

## Typische Prüfungsszenarien
- SIEM vs. Monitoring unterscheiden
- False Positive / False Negative erklären
- Reaktionskette bei Security Alert beschreiben

## Querverweise
[[Monitoring und SNMP]] · [[Ticketsysteme]] · [[Grundlagen der IT-Sicherheit im beruflichen Alltag]]
