# Relationale, nicht relationale & NoSQL Datenbanken

## Definition
Relationale DBs speichern Daten tabellarisch mit SQL; NoSQL umfasst dokumenten-, key-value-, spalten- oder graphorientierte Modelle.

## Warum ist das so?
Unterschiedliche Lastprofile: starke Konsistenz/komplexe Joins vs. horizontale Skalierung/flexible Schemata.

## Vergleich
| Kriterium | Relational | NoSQL |
|---|---|---|
| Schema | fest | flexibel |
| Transaktionen | stark (ACID) | oft BASE/variabel |
| Joins | sehr gut | je nach Typ eingeschränkt |
| Skalierung | eher vertikal + replizierbar | oft horizontal |

## Zusammenspiel
Hybride Architekturen sind üblich: relationale DB für Kerntransaktionen, NoSQL für Logs/Caching.

## Beispielaufgabe
**Frage:** Wann ist ein Dokumentenspeicher sinnvoll?

**Lösung:** Bei variablen, verschachtelten Datenstrukturen mit hoher Schreib-/Lese-Last (z. B. Produktkatalog).
