# Statische und dynamischen Testverfahren

Um Fehler (Bugs) oder Sicherheitslücken in IT-Systemen und Code zu finden, unterscheidet man grundsätzlich zwei Testansätze.

**1. Statische Testverfahren:**
Der Code (oder die Konfiguration) wird **nicht** ausgeführt. Er wird lediglich gelesen und analysiert.
- *Manuelle Prüfung:* Code-Reviews (Entwickler lesen den Code ihrer Kollegen) oder Walkthroughs.
- *Automatisierte Prüfung:* Tools zur statischen Code-Analyse (Linter) prüfen den Text auf Syntaxfehler, Sicherheitslücken (z. B. unsichere SQL-Queries, siehe [[SQL Befehle Aufbau, Arten und JOINs]]) oder Verstöße gegen Programmierrichtlinien.
- *Vorteil:* Man findet Fehler extrem früh im Prozess, noch bevor das Programm überhaupt lauffähig ist.

**2. Dynamische Testverfahren:**
Das Programm (oder Skript) wird **ausgeführt**. 
- Hierbei wird das Verhalten des Systems zur Laufzeit getestet, indem man Eingabedaten übergibt und prüft, ob die erwarteten Ausgabedaten geliefert werden.
- Dazu gehören [[Testvarianten Unit-Tests, Integrationstests, Systemtests....|Unit-Tests, Integrationstests und Systemtests]].
- Man unterscheidet hierbei oft zwischen **Black-Box-Tests** (der Tester kennt den internen Code nicht und testet nur die UI/Schnittstelle) und **White-Box-Tests** (der Tester kennt die innere Logik des Codes).

Querverweise: [[Testvarianten Unit-Tests, Integrationstests, Systemtests....]], [[Debugging]].
