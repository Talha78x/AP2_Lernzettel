# Pseudocode

## Definition
Pseudocode beschreibt Algorithmen in strukturierter, sprachneutraler Form.

## Warum ist das so?
Er trennt Problemlösung von Syntaxdetails und hilft Kommunikation zwischen Fachseite und Entwicklung.

## Zusammenspiel
Pseudocode ist Brücke zwischen [[UML Diagramme]] und Implementierung in [[Programmiersprachen]].

## Beispiel
```text
EINGABE note
WENN note >= 50 DANN
    AUSGABE "bestanden"
SONST
    AUSGABE "nicht bestanden"
ENDEWENN
```

## Prüfungsaufgabe
**Aufgabe:** Formuliere eine Schleife, die Summen 1..n bildet.

**Lösung:**
```text
summe <- 0
FÜR i <- 1 BIS n
  summe <- summe + i
ENDEFÜR
AUSGABE summe
```

**Rechenbeispiel:** n=4 -> 1+2+3+4=10.
