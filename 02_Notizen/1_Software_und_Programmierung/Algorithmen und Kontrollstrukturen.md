# Algorithmen und Kontrollstrukturen

Ein **Algorithmus** ist eine eindeutige Handlungsvorschrift zur Lösung eines Problems. Er besteht aus endlich vielen, wohldefinierten Einzelschritten. Im IT-Alltag begegnen uns Algorithmen ständig, z. B. als Sortieralgorithmus (Bubble Sort) oder bei der Suche in einem [[Active Directory und LDAP|Verzeichnisdienst]].

Um die Logik eines Algorithmus zu steuern, benötigt man **Kontrollstrukturen**. Sie legen fest, in welcher Reihenfolge die Anweisungen abgearbeitet werden. Die drei Grundbausteine (die oft im [[Pseudocode]] oder in [[UML Diagramme|Aktivitätsdiagrammen]] dargestellt werden) sind:

1. **Sequenz:**
   Die einfache, lineare Ausführung von Befehlen nacheinander.
2. **Selektion (Verzweigung / Bedingung):**
   Eine Fallunterscheidung. Ein Codeblock wird nur ausgeführt, wenn eine bestimmte Bedingung wahr ist.
   *Beispiel:* `IF (Passwort == richtig) THEN Login() ELSE Abbruch()`
3. **Iteration (Schleife):**
   Eine Anweisung wird so lange wiederholt, bis eine Abbruchbedingung erfüllt ist (oder für eine fest definierte Anzahl von Durchläufen).
   *Beispiel:* `WHILE`, `FOR`, `DO-UNTIL`

In Prüfungen wird oft verlangt, aus einer Textvorgabe heraus die passenden Kontrollstrukturen zu wählen (z.B. "Überprüfe für alle 100 User in der CSV-Datei... -> FOR-Schleife").

Querverweise: [[Programmierparadigmen prozedural, objektorientiert, funktional, deklarativ]], [[Skript- und Shellprogrammierung]].
