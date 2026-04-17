# Testvarianten Unit-Tests, Integrationstests, Systemtests....

In der IT (besonders in der Anwendungsentwicklung, aber auch relevant für FISIs beim Scripting oder System-Rollout) wird Software auf verschiedenen Ebenen getestet. Man spricht oft von der **Testpyramide**.

1. **Unit-Tests (Komponententests):**
   Das Fundament der Testpyramide. Hier wird die kleinstmögliche Einheit (z. B. eine einzelne Methode oder [[Programmierparadigmen prozedural, objektorientiert, funktional, deklarativ|Funktion]]) isoliert getestet. Sie sind schnell, billig und werden meist vom Entwickler selbst geschrieben (oft als White-Box-Test).
   
2. **Integrationstests:**
   Hier wird überprüft, ob verschiedene (zuvor einzeln getestete) Module oder Komponenten korrekt zusammenarbeiten. Der Fokus liegt auf den Schnittstellen (z. B. kommuniziert die Web-App richtig mit der [[Relationale, nicht relationale NoSQL Datenbanken|Datenbank]]?). Fehlerbehebungen sind hier schon komplexer.

3. **Systemtests:**
   Die Software wird als komplettes, integriertes Gesamtsystem in einer Umgebung getestet, die der späteren Produktionsumgebung sehr ähnlich ist. Hier wird geprüft, ob die fachlichen Anforderungen aus dem [[Pflichtenheft]] erfüllt werden (meist als Black-Box-Test durch separate Tester).

4. **Akzeptanztests (Abnahmetests):**
   Der letzte Schritt. Der Endkunde (oder Fachbereich) testet das System, um zu entscheiden, ob er es abnimmt und bezahlt.

Querverweise: [[TDD, PDCA, KVP, Kennzahlen und Soll-Ist-Vergleich]], [[Statische und dynamischen Testverfahren]].
