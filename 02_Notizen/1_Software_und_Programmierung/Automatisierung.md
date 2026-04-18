# Automatisierung

## Definition
Automatisierung bedeutet, wiederkehrende Prozesse mit Skripten, Jobs oder Workflows ohne manuelle Einzelschritte auszuführen.

## Warum ist das so?
Wiederholte manuelle Arbeit ist fehleranfällig, langsam und teuer. Automatisierung erhöht Qualität, Geschwindigkeit und Nachvollziehbarkeit.

## Zusammenspiel
- Umsetzung über [[Skript- und Shellprogrammierung]].
- Fachliche Logik basiert auf [[Algorithmen und Kontrollstrukturen]].
- Qualitätssicherung erfolgt durch Tests und Logs.

## Eigene Worte
„Automatisierung heißt: Einmal sauber denken, dann tausendmal korrekt ausführen lassen.“

## Automatisierungsarten
| Art | Beispiel | Nutzen |
|---|---|---|
| Zeitgesteuert | nächtliches Backup | Entlastung Team |
| Ereignisgesteuert | Ticket erstellt -> User anlegen | schnellere Reaktion |
| CI/CD | Build + Tests bei Git-Push | weniger Integrationsfehler |

## Beispielaufgabe mit Lösung
**Aufgabe:** Täglicher Log-Export (300 MB/Tag) soll 30 Tage aufbewahrt werden. Benötigter Speicher?

**Rechenweg:**
`300 MB * 30 = 9000 MB = 9 GB` (ohne Kompression).

Mit 40% Kompression: `9 GB * 0.6 = 5.4 GB`.

## Prüfungsszenarien
- Prozess analysieren und Automatisierungspotenzial begründen.
- Vor-/Nachteile (Sicherheit, Wartung, Monitoring) erläutern.
