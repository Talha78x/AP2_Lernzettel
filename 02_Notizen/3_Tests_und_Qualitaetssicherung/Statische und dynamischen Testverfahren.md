# Statische und dynamischen Testverfahren

## Definition
Bei **statischen Testverfahren** wird ein Artefakt geprüft, **ohne** dass das System ausgeführt wird. Geprüft werden zum Beispiel Quellcode, Konfigurationen, SQL-Skripte, Dokumentationen oder Architekturmodelle.

Bei **dynamischen Testverfahren** wird das System oder ein Teil davon **ausgeführt**, um sein Verhalten mit erwarteten Ergebnissen zu vergleichen.

## Warum ist das so?
Nicht jeder Fehler zeigt sich erst zur Laufzeit:
- Syntax-, Stil- oder Sicherheitsprobleme erkennt man oft schon vorher.
- Logik-, Integrations- und Laufzeitfehler werden meist erst sichtbar, wenn Komponenten wirklich arbeiten.

Darum ergänzen sich beide Verfahren. Statische Tests verschieben die Fehlererkennung nach vorne, dynamische Tests prüfen das reale Verhalten.

## Zusammenspiel
- Statische Tests prüfen früh Codequalität, Wartbarkeit und Risiken.
- Dynamische Tests prüfen Funktionen, Schnittstellen und Fachlogik.
- [[Debugging]] beginnt oft dort, wo dynamische Tests fehlschlagen.
- [[Testvarianten (Unit-Tests, Integrationstests, Systemtests...)]] sind typische Ausprägungen dynamischer Tests.
- In [[Versionsmanagement (GIT, Repos) des Quellcodes]] werden beide oft in CI/CD-Pipelines automatisiert.

## Eigene Worte (prüfungsnah)
Statisches Testen ist wie Korrekturlesen, bevor ein Text veröffentlicht wird. Dynamisches Testen ist wie ein Probelauf unter echten Bedingungen. Beides zusammen ist nötig, weil man durch Lesen nicht jedes Laufzeitproblem erkennt und durch Ausführen nicht jede schlechte Struktur sieht.

## Gegenüberstellung
| Merkmal | Statisch | Dynamisch |
|---|---|---|
| Ausführung des Codes | Nein | Ja |
| Ziel | Fehler früh erkennen, Qualität sichern | Verhalten zur Laufzeit prüfen |
| Typische Objekte | Quellcode, Konfiguration, Doku | Programme, Module, Schnittstellen |
| Typische Werkzeuge | Linter, SAST, Code-Review | Testframeworks, Testdaten, Monitoring |
| Typische Fehler | Stilbruch, tote Variablen, Sicherheitsmuster | Falsche Ergebnisse, Abstürze, Timing-Probleme |
| Zeitpunkt | Sehr früh im Entwicklungsprozess | Nach oder während der Implementierung |

## Typische statische Testverfahren
| Verfahren | Beschreibung | Beispiel |
|---|---|---|
| Review | Menschen prüfen Code oder Dokumente | Vier-Augen-Prinzip vor Merge |
| Walkthrough | Autor erklärt den Ablauf schrittweise | Fachlogik mit Team durchgehen |
| Inspektion | Formalere Prüfung mit Rollen und Kriterien | Sicherheitskritische Änderungen |
| Linter | Prüft Syntax, Stil und bekannte Muster | Python-Linter findet ungenutzte Variablen |
| Statische Codeanalyse | Sucht Risiken oder Schwachstellen | Unsichere SQL-Strings oder Hardcoded Secrets |

## Typische dynamische Testverfahren
| Verfahren | Beschreibung | Beispiel |
|---|---|---|
| Funktionstest | Prüft fachlich richtige Ergebnisse | Rabattberechnung liefert korrekten Preis |
| Grenzwerttest | Prüft Randfälle | Alter `17`, `18`, `19` |
| Last-/Performancetest | Prüft Verhalten unter hoher Belastung | Viele API-Aufrufe gleichzeitig |
| Fehlertest | Prüft falsche oder fehlende Eingaben | Leeres Pflichtfeld, ungültige IP-Adresse |
| Regressionstest | Prüft, ob ein Fix andere Teile beschädigt | Login-Fix ohne Nebenwirkung auf MFA |

## Black Box und White Box
| Begriff | Bedeutung | Typischer Einsatz |
|---|---|---|
| Black-Box-Test | Interne Struktur unbekannt oder egal | Fachbereich testet Oberfläche oder API |
| White-Box-Test | Innere Struktur ist bekannt | Entwickler prüft Bedingungen, Pfade, Schleifen |
| Grey-Box-Test | Teilwissen über interne Struktur | Integration, Schnittstellen, Security |

## Beispielaufgabe mit Lösung
**Aufgabe:** Ordne die folgenden Prüfungen zu:
1. Ein Kollege liest einen SQL-Query und erkennt, dass Eingaben ungefiltert direkt in die Abfrage eingebaut werden.
2. Ein Tester startet die Anwendung und prüft, ob nach dem Login die Startseite erscheint.

**Lösung:**
1. **Statisches Testverfahren**, weil der Code geprüft wird, ohne ihn auszuführen.
2. **Dynamisches Testverfahren**, weil das System tatsächlich gestartet und benutzt wird.

**Prüfungsbegründung:**
Der entscheidende Unterschied ist nicht "automatisch oder manuell", sondern ob eine Ausführung stattfindet.

## Typische Prüfungsszenarien
- Unterschiede zwischen statisch und dynamisch in eigenen Worten erklären.
- Beispiele korrekt zuordnen.
- Vorteile statischer Tests im Entwicklungsprozess nennen.
- Begründen, warum statische Tests dynamische Tests nicht ersetzen können.

## Merksätze
- Statisch prüft das Artefakt, dynamisch prüft das Verhalten.
- Früh gefundene Fehler sind günstiger als spät gefundene Fehler.
- Gute Qualitätssicherung kombiniert beide Ansätze.
