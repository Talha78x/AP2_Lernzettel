# Algorithmen und Kontrollstrukturen

## Definition
Ein **Algorithmus** ist eine endliche, eindeutige und ausführbare Schrittfolge zur Lösung eines Problems.
**Kontrollstrukturen** legen fest, in welcher Reihenfolge Schritte ausgeführt werden (Sequenz, Auswahl, Wiederholung).

## Warum ist das so?
Programme müssen für Menschen planbar und für Rechner deterministisch sein. Kontrollstrukturen reduzieren Komplexität und vermeiden unkontrollierte Sprunglogik.

## Zusammenspiel
- Anforderungen aus [[Mock-Ups]] und [[Bildschirmausgabemasken]] definieren die fachlichen Abläufe.
- Die Abläufe werden als [[Pseudocode]] oder [[UML Diagramme]] modelliert.
- Danach erfolgt die Umsetzung in [[Programmiersprachen]] unter Nutzung passender [[Programmierparadigmen (prozedural, objektorientiert, funktional, deklarativ)]].

## Eigene Worte (prüfungsnah)
„Ein Algorithmus ist wie ein Kochrezept: klare Schritte, klare Reihenfolge, klares Ergebnis. Kontrollstrukturen sind die Regeln, wann welcher Schritt dran ist.“

## Kernbausteine
| Struktur | Zweck | Beispiel |
|---|---|---|
| Sequenz | Schritte nacheinander | `lesen -> prüfen -> speichern` |
| Verzweigung | Alternative Wege | `if score >= 50 then bestanden` |
| Schleife | Wiederholung | `while eingabe falsch` |

## Beispielaufgabe mit Lösung
**Aufgabe:** Ein Shop gibt 10% Rabatt ab 100 EUR. Sonst 0%. Berechne Endpreis.

**Lösung (Denkschritte):**
1. Eingabe: Warenwert `w`.
2. Verzweigung: wenn `w >= 100`, dann `rabatt = 0.10*w`, sonst `rabatt = 0`.
3. Ausgabe: `endpreis = w - rabatt`.

```text
w = 120
rabatt = 12
endpreis = 108
```

## Typische Prüfungsszenarien
- Ablaufdiagramm in Pseudocode übersetzen.
- Schleifenfehler finden (Off-by-one).
- Zeitkomplexität grob vergleichen (linear vs. quadratisch).
