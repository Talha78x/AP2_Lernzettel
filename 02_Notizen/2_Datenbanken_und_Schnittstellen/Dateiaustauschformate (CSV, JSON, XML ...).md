# Dateiaustauschformate (CSV, JSON, XML ...)

## Definition
Austauschformate standardisieren, wie Daten systemübergreifend gespeichert/übertragen werden.

## Warum ist das so?
Ohne einheitliches Format entstehen Medienbrüche und Parsing-Fehler.

## Vergleich
| Format | Stärken | Schwächen | Typisch |
|---|---|---|---|
| CSV | einfach, klein | keine Hierarchie | Tabellenexport |
| JSON | leichtgewichtig, API-Standard | kein Schema erzwungen | Web/APIs |
| XML | streng, validierbar (XSD) | verbose | Enterprise/Legacy |

## Beispielaufgabe
**Aufgabe:** Wann CSV ungeeignet?

**Lösung:** Bei verschachtelten Daten (Adresse mit Listen), da CSV keine echte Hierarchie abbildet.
