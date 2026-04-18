# TDD, PDCA, KVP, Kennzahlen und Soll-Ist-Vergleich

## Definition
Diese Begriffe gehören zur strukturierten Qualitätsverbesserung:

- **TDD (Test-Driven Development):** Entwicklungsmethode, bei der zuerst ein fehlschlagender Test geschrieben wird, dann der minimale Code für das Bestehen des Tests und anschließend Refactoring erfolgt.
- **PDCA (Plan, Do, Check, Act):** Regelkreis zur systematischen Verbesserung von Prozessen.
- **KVP (Kontinuierlicher Verbesserungsprozess):** Haltung und Vorgehen, Verbesserungen regelmäßig und dauerhaft umzusetzen.
- **Kennzahlen (KPIs):** Messgrößen zur Bewertung von Qualität, Zeit, Kosten oder Leistung.
- **Soll-Ist-Vergleich:** Gegenüberstellung zwischen geplantem Zielwert und tatsächlich erreichtem Wert.

## Warum ist das so?
Qualität entsteht nicht nur durch "am Ende testen". In IT-Projekten braucht man:
- klare Ziele
- messbare Ergebnisse
- nachvollziehbare Verbesserungen
- Rückkopplung bei Abweichungen

Ohne Messung bleibt Qualität ein Bauchgefühl. Ohne Methode werden Fehler nur punktuell behoben, aber Prozesse nicht wirklich besser.

## Zusammenspiel
| Baustein | Rolle im Zusammenspiel |
|---|---|
| TDD | verbessert Codequalität direkt während der Entwicklung |
| PDCA | strukturiert Verbesserungsmaßnahmen als Regelkreis |
| KVP | macht Verbesserung zur dauerhaften Gewohnheit |
| Kennzahlen | liefern objektive Messwerte |
| Soll-Ist-Vergleich | zeigt Abweichungen und Handlungsbedarf |

Beispiel: Ein Team will die Fehlerrate senken. Es plant Maßnahmen (`Plan`), führt zusätzliche Tests ein (`Do`), misst Defektrate und Durchlaufzeit (`Check`) und übernimmt erfolgreiche Regeln als Standard (`Act`). Wenn das regelmäßig passiert, lebt das Team KVP.

## Eigene Worte (prüfungsnah)
TDD ist eine Arbeitsweise für Entwickler. PDCA ist ein Verbesserungsregelkreis für Prozesse. KVP ist die langfristige Denkweise dahinter. Kennzahlen und Soll-Ist-Vergleich liefern die Zahlen, mit denen man prüfen kann, ob eine Maßnahme wirklich etwas gebracht hat.

## TDD im Detail
### Red-Green-Refactor
| Phase | Bedeutung | Typische Frage |
|---|---|---|
| Red | Test schlägt fehl | Was soll das System können? |
| Green | Minimaler Code macht Test grün | Wie erreiche ich das kleinste funktionierende Ergebnis? |
| Refactor | Code verbessern, Verhalten beibehalten | Wie wird die Lösung sauberer und wartbarer? |

**Warum ist TDD hilfreich?**
- Anforderungen werden präziser formuliert.
- Code wird testbarer und meist modularer.
- Regressionen fallen schneller auf.

## PDCA und KVP
| Schritt | Leitfrage | Beispiel aus der IT |
|---|---|---|
| Plan | Was wollen wir verbessern? | Login-Fehlerquote soll von 4 % auf 1 % sinken |
| Do | Welche Maßnahme setzen wir um? | Validierung, Tests und Monitoring erweitern |
| Check | Was ist das Ergebnis? | Fehlerquote nach 2 Wochen messen |
| Act | Was lernen wir daraus? | Maßnahme als Standard übernehmen oder anpassen |

KVP bedeutet, dass dieser Kreislauf nicht einmalig, sondern dauerhaft angewandt wird.

## Kennzahlen und Soll-Ist-Vergleich
| Kennzahl | Soll | Ist | Aussage |
|---|---|---|---|
| Fehlerrate pro Release | max. 5 Bugs | 8 Bugs | Ziel verfehlt |
| Antwortzeit API | max. 300 ms | 240 ms | Ziel erreicht |
| Ticket-Lösungszeit | max. 8 h | 11 h | Prozess verbessern |
| Testabdeckung | min. 70 % | 76 % | Ziel erreicht |

**Wichtig für die Prüfung:** Eine Kennzahl allein genügt nicht. Erst durch Sollwert, Messung und Bewertung entsteht ein sinnvoller Soll-Ist-Vergleich.

## Beispielaufgabe mit Lösung
**Aufgabe:** Ein Team definiert als Soll: "Die mittlere Ticket-Lösungszeit soll höchstens 6 Stunden betragen." Nach einer Woche liegt der gemessene Ist-Wert bei 7,5 Stunden. Welche Aussage ist richtig und welcher PDCA-Schritt folgt?

**Lösung:**
1. **Soll-Ist-Vergleich:** `7,5 h > 6 h`, also ist das Ziel **nicht erreicht**.
2. Das gehört in den PDCA-Schritt **Check**, weil Ergebnisse gemessen und bewertet werden.
3. Danach folgt **Act**:
   - Ursachen analysieren
   - Maßnahmen anpassen
   - neuen Zyklus starten

**Prüfungsnahe Formulierung:**
Der Soll-Ist-Vergleich zeigt eine negative Abweichung von `1,5 Stunden`. Daraus ergibt sich Verbesserungsbedarf im Prozess.

## Typische Prüfungsszenarien
- TDD von klassischen Testphasen abgrenzen.
- PDCA-Reihenfolge korrekt angeben.
- KPIs sinnvoll auswählen, zum Beispiel Verfügbarkeit, Durchlaufzeit oder Defektrate.
- Einen Soll-Ist-Vergleich rechnen und interpretieren.
- KVP als dauerhafte Verbesserungskultur erklären.

## Querverbindungen
- [[Testvarianten (Unit-Tests, Integrationstests, Systemtests...)]] liefern Messpunkte für TDD und Qualitätskontrolle.
- [[Debugging]] hilft, negative Abweichungen technisch zu beheben.
- [[Projektcontrolling]] und [[Abschlussbericht]] nutzen Soll-Ist-Vergleiche im Projektkontext.
- [[SLA]] nutzt ebenfalls Kennzahlen, etwa für Reaktions- und Lösungszeiten.

## Merksätze
- TDD ist eine Entwicklungsdisziplin, PDCA ein Verbesserungszyklus.
- KVP bedeutet: verbessern ist kein Einzelereignis, sondern Routine.
- Nur Messbares lässt sich sauber vergleichen und steuern.
