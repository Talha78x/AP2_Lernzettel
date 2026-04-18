# ER-Modell (Attribute, Beziehungen, Kardinalitäten, referenzielle Integrität)

## Definition
Das ER-Modell beschreibt fachliche Datenobjekte (Entitäten), deren Eigenschaften (Attribute) und Beziehungen.

## Warum ist das so?
Sauberes Datenmodell verhindert Redundanz, Anomalien und inkonsistente Daten.

## Zusammenspiel
ER-Modell -> Relationenmodell -> [[SQL Befehle (Aufbau, Arten und JOINs)]] -> Normalisierung.

## Kardinalitäten
| Beziehung | Bedeutung |
|---|---|
| 1:1 | z. B. Person <-> Personalakte |
| 1:n | Kunde <-> Bestellung |
| n:m | Student <-> Kurs (Zwischentabelle nötig) |

## Beispielaufgabe
**Aufgabe:** Warum braucht n:m eine Zwischentabelle?

**Lösung:** Relationale Tabellen können n:m nicht direkt speichern; Zwischentabelle enthält zwei Fremdschlüssel.
