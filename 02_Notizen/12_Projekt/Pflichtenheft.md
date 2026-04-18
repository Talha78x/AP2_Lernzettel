# Pflichtenheft

## Definition
Das **Pflichtenheft** beschreibt aus Auftragnehmersicht **wie** die Anforderungen des Lastenhefts umgesetzt werden.

## Warum ist das so?
Es schafft Verbindlichkeit für Architektur, Schnittstellen, Tests und Abnahme.

## Zusammenspiel
[[Lastenheft]] liefert Anforderungen, Pflichtenheft konkretisiert Umsetzung, Tests und Lieferobjekte.

## Inhalte
| Bereich | Beispiel |
|---|---|
| Architektur | 3-Tier-Anwendung mit Reverse Proxy |
| Schnittstellen | REST-API mit OAuth2 |
| Qualität | Antwortzeit < 300 ms |
| Test/Abnahme | Lasttest mit 200 Usern |

## Beispielaufgabe
Wenn im Lastenheft "hohe Verfügbarkeit" steht, konkretisiert das Pflichtenheft z. B. "99,9 % Verfügbarkeit, redundanter LB".
