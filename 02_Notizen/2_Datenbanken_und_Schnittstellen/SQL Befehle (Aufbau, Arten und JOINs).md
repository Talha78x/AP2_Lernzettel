# SQL Befehle (Aufbau, Arten und JOINs)

## Definition
SQL ist die Standardsprache zur Definition, Abfrage und Manipulation relationaler Daten.

## Warum ist das so?
Daten müssen konsistent gespeichert und effizient abgefragt werden; SQL ist deklarativ und optimierbar.

## Aufbau
- **DDL:** `CREATE`, `ALTER`, `DROP`
- **DML:** `INSERT`, `UPDATE`, `DELETE`
- **DQL:** `SELECT`
- **DCL/TCL:** `GRANT`, `REVOKE`, `COMMIT`, `ROLLBACK`

## JOINs im Zusammenspiel
| JOIN | Ergebnis |
|---|---|
| INNER JOIN | nur Treffer in beiden Tabellen |
| LEFT JOIN | alle links + passende rechts |
| RIGHT JOIN | alle rechts + passende links |
| FULL OUTER JOIN | alle aus beiden Seiten |

## Beispielaufgabe mit Lösung
**Aufgabe:** Liste alle Kunden mit Bestellanzahl (auch ohne Bestellung).

```sql
SELECT k.kunden_id, k.name, COUNT(b.bestell_id) AS anzahl
FROM kunden k
LEFT JOIN bestellung b ON b.kunden_id = k.kunden_id
GROUP BY k.kunden_id, k.name
ORDER BY anzahl DESC;
```

**Warum LEFT JOIN?**
Damit Kunden ohne Bestellung mit `anzahl = 0` erscheinen.
