# 1st-Level, 2nd-Level, 3rd-Level-Support

## Definition
Support-Level strukturieren den IT-Support nach **Komplexität, Verantwortlichkeit und Eskalationsweg**:
- **1st-Level**: Annahme, Vorqualifizierung, Standardlösungen
- **2nd-Level**: technische Vertiefung, System- und Fachwissen
- **3rd-Level**: Hersteller-/Entwickler-Niveau, tiefste Analyse

## Warum ist das so?
Nicht jede Störung braucht sofort Expertenzeit. Die Staffelung senkt Kosten, verkürzt Wartezeiten und sorgt für klare Zuständigkeiten.

## Zusammenspiel im Betrieb
1. Meldung kommt über [[Ticketsysteme]].
2. 1st-Level prüft Priorität, Kategorie, bekannte Lösung (KEDB/FAQ).
3. Falls ungelöst: Eskalation an 2nd-Level mit vollständiger Dokumentation.
4. Bei Produktfehlern oder Code-Themen: 3rd-Level.
5. Rückmeldung + Lösung fließen in [[SOP]] und Wissensdatenbank zurück.

## Typische Tätigkeiten pro Level
| Level | Fokus | Beispiele |
|---|---|---|
| 1st | Schnelle Wiederherstellung | Passwort-Reset, VPN-Profil, Druckerfehler |
| 2nd | Technische Ursachenanalyse | AD-Replikation, DNS-Fehler, Patch-Konflikte |
| 3rd | Architektur/Code/Hersteller | Bugfix, Firmware-Eskalation, Hotfix |

## Eigene Worte (prüfungsnah)
Der 1st-Level ist das „Frontdesk“, der 2nd-Level die „Werkstatt“ und der 3rd-Level die „Entwicklung“. Wichtig in Prüfungen: **Eskalation bedeutet nicht abschieben**, sondern strukturiert übergeben.

## Beispielaufgabe mit Lösung
**Aufgabe:** Ein Benutzer kann nicht drucken. 1st-Level prüft Kabel, Treiber, Queue-Neustart ohne Erfolg. Was ist der nächste Schritt?

**Lösung:**
- Ticket mit bisheriger Diagnose, Zeitstempel und Logs an 2nd-Level eskalieren.
- Priorität bleibt abhängig vom Geschäftsimpact (z. B. Buchhaltung am Monatsende = höher).

## Typische Prüfungsszenarien
- „Welcher Level ist zuständig?“
- Unterschied Incident vs. Problem im Eskalationskontext
- Welche Informationen müssen beim Eskalieren mitgegeben werden

## Querverweise
[[Ticketsysteme]] · [[SLA]] · [[Troubleshooting und Härtungsmaßnahmen]] · [[SOP]]
