# Debugging

**Debugging** ist der systematische Prozess des Findens und Behebens von Fehlern (Bugs) in Computerprogrammen, [[Skript- und Shellprogrammierung|Skripten]] oder Hardware-Setups. 

Während Tests (siehe [[Statische und dynamischen Testverfahren]]) dazu da sind, festzustellen, *dass* ein Fehler existiert, dient das Debugging dazu, herauszufinden, *warum* der Fehler auftritt und *wo* genau im Code er sich versteckt.

**Typische Werkzeuge und Methoden:**
- **Debugger:** Ein Software-Tool (meist in der Entwicklungsumgebung integriert), mit dem man ein Programm anhalten (**Breakpoint / Haltepunkt**) und dann Zeile für Zeile im Schrittmodus (Single-Stepping) ausführen kann. Dabei kann man sich live ansehen, welche Werte bestimmte Variablen in diesem Moment haben.
- **Logging / Print-Debugging:** An kritischen Stellen im Code werden Ausgaben (Log-Files oder Konsolen-Prints) eingebaut, um zu sehen, ob das Programm diesen Punkt überhaupt erreicht hat und welche Daten es verarbeitet. (Sehr wichtig im FISI-Alltag beim Skripting).
- **Rubber Duck Debugging:** Eine Methode, bei der der Entwickler sein Problem (oder seinen Code Zeile für Zeile) einer unbelebten Ente auf dem Schreibtisch erklärt. Das bloße laute Formulieren der Logik führt oft dazu, dass man den Denkfehler selbst erkennt.

Querverweise: [[Statische und dynamischen Testverfahren]], [[Troubleshooting und Hartungsmanahmen]].
