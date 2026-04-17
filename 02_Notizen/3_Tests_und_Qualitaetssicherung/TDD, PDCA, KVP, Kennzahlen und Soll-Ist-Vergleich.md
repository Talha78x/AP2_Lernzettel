# TDD, PDCA, KVP, Kennzahlen und Soll-Ist-Vergleich

Qualitätssicherung ist ein zentraler Aspekt der IT, sowohl bei der Softwareentwicklung als auch beim IT-Betrieb. In der IHK-Projektdokumentation wird oft ein Soll-Ist-Vergleich gefordert.

**PDCA-Zyklus (Demingkreis):**
Ein iterativer Problemlösungsprozess, der in vier Phasen abläuft:
1. **Plan:** Problem analysieren, Ziele definieren, Maßnahmen planen (den "Soll"-Zustand festlegen).
2. **Do:** Die geplanten Maßnahmen (oft erst im kleinen Rahmen) umsetzen.
3. **Check:** Ergebnisse überprüfen. Hier findet der **Soll-Ist-Vergleich** statt (Wurden die Ziele erreicht?).
4. **Act (Adjust):** Bei Erfolg die Maßnahme als neuen Standard im Unternehmen etablieren. Bei Misserfolg den Prozess anpassen und den Zyklus neu starten.

**KVP (Kontinuierlicher Verbesserungsprozess):**
Eine Unternehmensphilosophie, die auf dem PDCA-Zyklus basiert. Das Ziel ist es, stetig kleine Verbesserungen in Qualität, Kosten und Zeit zu erreichen, anstatt nur auf große, sprunghafte Innovationen zu setzen.

**Kennzahlen (KPIs) und Soll-Ist-Vergleich:**
Um im "Check"-Schritt messen zu können, ob man erfolgreich war, braucht man KPIs (Key Performance Indicators) – zum Beispiel "Ausfallzeit der Server" oder "Anzahl der Bugs pro Release". Beim Soll-Ist-Vergleich wird der zuvor definierte Zielwert (Soll) dem tatsächlich gemessenen Wert (Ist) gegenübergestellt.

**TDD (Test-Driven Development):**
Ein Ansatz aus der Softwareentwicklung. Man schreibt *zuerst* einen fehlgeschlagenen automatisierten Test (siehe [[Testvarianten Unit-Tests, Integrationstests, Systemtests....]]), schreibt dann genau so viel Programmcode, bis der Test bestanden wird, und optimiert den Code anschließend (Refactoring).

Querverweise: [[Abschlussbericht]], [[Projektcontrolling]], [[SLA]].
