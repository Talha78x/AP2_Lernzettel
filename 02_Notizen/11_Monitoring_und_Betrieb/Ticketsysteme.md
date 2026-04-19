# Ticketsysteme

## Definition
Ein Ticketsystem ist das zentrale Werkzeug zur strukturierten Erfassung, Priorisierung, Bearbeitung und Dokumentation von Supportfällen.

## Warum ist das so?
Ohne Ticketing gehen Informationen verloren, Verantwortlichkeiten sind unklar und SLA-Nachweise fehlen.

## Zusammenspiel
- Alarme aus [[Monitoring und SNMP]] erzeugen Tickets.
- Priorität steuert die Bearbeitungsreihenfolge.
- Übergabe zwischen [[1st-Level, 2nd-Level, 3rd-Level-Support]] erfolgt nachvollziehbar.
- Abschlussdokumentation verbessert künftige [[SOP]].

## Ticket-Lebenszyklus
| Status | Zweck |
|---|---|
| Neu | Eingang erfasst |
| In Bearbeitung | Analyse läuft |
| Warten auf Kunde | Rückfrage/Bestätigung offen |
| Eskaliert | Übergabe an höheren Level |
| Gelöst | Lösung umgesetzt |
| Geschlossen | Kunde bestätigt/Frist abgelaufen |

## Priorisierung (typisch)
**Priorität = Auswirkung × Dringlichkeit**
- Hohe Auswirkung + hohe Dringlichkeit = P1
- Geringe Auswirkung + geringe Dringlichkeit = P4

## Beispielaufgabe
**Aufgabe:** VPN-Ausfall für alle Standorte um 08:00 Uhr. Einzelnutzer-Druckerproblem um 08:05 Uhr. Welche Reihenfolge?  
**Lösung:** VPN zuerst (hohe Auswirkung, hohe Dringlichkeit), Drucker danach.

## Typische Prüfungsszenarien
- Incident/Service Request unterscheiden
- Pflichtfelder im Ticket nennen
- SLA-Zeitmessung im Ticketfluss erklären

## Querverweise
[[SLA]] · [[SOP]] · [[Troubleshooting und Härtungsmaßnahmen]]
