# Debugging

## Definition
**Debugging** ist das systematische Eingrenzen, Analysieren und Beheben eines Fehlers in Software, Skripten oder Konfigurationen. Tests zeigen oft nur, **dass** etwas nicht funktioniert. Debugging klärt zusätzlich, **wo** der Fehler entsteht, **warum** er entsteht und **unter welchen Bedingungen** er reproduzierbar ist.

## Warum ist das so?
Ein Fehler ist selten "zufällig". Meist steckt eine klare Ursache dahinter:
- falsche Eingabedaten
- fehlerhafte Programmlogik
- unpassende Schnittstellen zwischen Komponenten
- falsche Annahmen über Zustände, Reihenfolgen oder Umgebungen

In Prüfungen ist genau das wichtig: Nicht nur "Bug gefunden", sondern nachvollziehbar begründen, an welcher Stelle Ursache und Wirkung zusammenhängen.

## Zusammenspiel
- [[Statische und dynamischen Testverfahren]] helfen, Fehler früh zu entdecken.
- [[Testvarianten (Unit-Tests, Integrationstests, Systemtests...)]] zeigen, auf welcher Ebene der Fehler auftritt.
- [[TDD, PDCA, KVP, Kennzahlen und Soll-Ist-Vergleich]] sorgt dafür, dass Fehlerbehebung nicht chaotisch, sondern messbar erfolgt.
- [[Versionsmanagement (GIT, Repos) des Quellcodes]] dokumentiert den Fix nachvollziehbar über Branches, Commits und Reviews.
- Im Betrieb überschneidet sich Debugging oft mit [[Troubleshooting und Härtungsmaßnahmen]].

## Eigene Worte (prüfungsnah)
Debugging ist Detektivarbeit mit Methode. Ich beobachte ein falsches Verhalten, grenze den Fehler ein, prüfe Annahmen, messe Zwischenergebnisse und bestätige erst dann die Ursache. Ein guter Debugger ändert nicht sofort zehn Dinge gleichzeitig, sondern arbeitet Schritt für Schritt.

## Typischer Ablauf
| Schritt | Frage | Typische Aktion |
|---|---|---|
| Fehlerbild erfassen | Was genau ist kaputt? | Meldung, Screenshot, Logeintrag, Zeitpunkt notieren |
| Reproduzierbarkeit prüfen | Tritt es immer oder nur manchmal auf? | Testfall mit gleicher Eingabe wiederholen |
| Fehler eingrenzen | Frontend, Backend, DB oder Netzwerk? | Logs, Breakpoints, Vergleich mit funktionierendem Fall |
| Ursache prüfen | Warum weicht der Zustand ab? | Variablenwerte, Rückgabewerte, Reihenfolge kontrollieren |
| Fix umsetzen | Wie wird die Ursache behoben? | Code, Konfiguration oder Daten korrigieren |
| Absichern | Ist nur dieser Fehler weg oder entstehen neue? | Regressionstest, Review, Dokumentation |

## Wichtige Methoden und Werkzeuge
| Methode | Wie funktioniert sie? | Vorteil | Typischer Prüfungsbezug |
|---|---|---|---|
| Breakpoints im Debugger | Programm an definierter Stelle anhalten | Zustände zur Laufzeit sichtbar | Variablenwert vor/nach `if` oder Schleife prüfen |
| Step Into / Over / Out | Schrittweise Ausführung | Kontrollfluss verstehen | Verzweigungen und Funktionsaufrufe analysieren |
| Logging | Zustände in Logdatei oder Konsole schreiben | Auch auf Servern und in Skripten nutzbar | Fehlerzeitpunkt und Datenfluss dokumentieren |
| Print-Debugging | Zusätzliche Ausgaben direkt im Code | Schnell und einfach | Häufig in Shell- oder kleinen Python-Skripten |
| Vergleich funktionierend vs. defekt | Soll-Zustand mit Ist-Zustand vergleichen | Ursachen schneller eingrenzen | Soll-Ist-Denke in Prüfung und Praxis |
| Rubber-Duck-Debugging | Logik laut erklären | Denkfehler werden sichtbar | Gut für algorithmische Aufgaben |

## Häufige Fehlerursachen
| Fehlerart | Beispiel |
|---|---|
| Off-by-one | Schleife läuft einen Schritt zu viel oder zu wenig |
| Null-/Leerwertproblem | Variable ist nicht gesetzt, Abfrage aber erwartet Inhalt |
| Datentypfehler | Text wird wie Zahl verarbeitet |
| Reihenfolgefehler | Funktion wird aufgerufen, bevor Daten geladen sind |
| Schnittstellenfehler | API liefert anderes Feldformat als erwartet |
| Umgebungsfehler | Pfad, Port, Berechtigung oder Version stimmt nicht |

## Beispielaufgabe mit Lösung
**Aufgabe:** Ein Skript soll nur Benutzer mit `alter >= 18` freischalten. Nutzer mit Alter `18` werden aber abgelehnt.

```python
if alter > 18:
    freigabe = True
else:
    freigabe = False
```

**Analyse:**
1. Fehlerbild: Benutzer mit `18` werden nicht freigeschaltet.
2. Reproduktion: Test mit `alter = 18`.
3. Beobachtung: Bedingung `alter > 18` ist für `18` falsch.
4. Ursache: Fachliche Anforderung lautet "ab 18", Code prüft aber "größer als 18".

**Lösung:**
```python
if alter >= 18:
    freigabe = True
else:
    freigabe = False
```

**Warum ist das die richtige Lösung?**
`>=` schließt den Grenzwert `18` ein. Genau solche Grenzwerte sind typische Prüfungsfallen.

## Typische Prüfungsszenarien
- Einen kleinen Codeausschnitt lesen und den Logikfehler benennen.
- Erklären, warum Logging in der Produktion oft praktischer als ein lokaler Debugger ist.
- Unterschied zwischen Testen und Debugging erläutern.
- Vorgehen beschreiben, wenn ein Fehler nur sporadisch auftritt.

## Merksätze
- Testen findet Fehler, Debugging erklärt Fehler.
- Erst reproduzieren, dann ändern.
- Ein Fix ohne Regressionstest ist noch keine saubere Fehlerbehebung.
