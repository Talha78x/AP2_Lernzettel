# Normalisierung Regeln

## Definition
Normalisierung strukturiert relationale Tabellen in Normalformen, um Redundanzen und Änderungsanomalien zu reduzieren.

## Warum ist das so?
Doppelt gespeicherte Daten führen zu Inkonsistenzen (Update-, Insert-, Delete-Anomalie).

## Normalformen
| Normalform | Kernaussage |
|---|---|
| 1NF | atomare Werte, keine Wiederholungsgruppen |
| 2NF | keine partiellen Abhängigkeiten vom Primärschlüssel |
| 3NF | keine transitiven Abhängigkeiten |

## Beispielaufgabe
**Aufgabe:** Tabelle `Bestellung(BestellID, KundeName, KundePLZ, Produkt, Preis)` in 3NF überführen.

**Lösungsskizze:**
- `Kunde(KundeID, Name, PLZ)`
- `Bestellung(BestellID, KundeID, Datum)`
- `Bestellposition(BestellID, ProduktID, Menge, Preis)`
