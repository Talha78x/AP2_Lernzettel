# Versionsmanagement (GIT, Repos) des Quellcodes

## Definition
**Versionsmanagement** verwaltet Änderungen an Dateien nachvollziehbar über die Zeit. In der IT ist dafür **Git** der De-facto-Standard. Es speichert nicht nur den aktuellen Stand, sondern auch die Entwicklungsschritte, Verantwortlichkeiten und Zusammenführungen.

Ein **Repository** ist dabei der Speicherort mit Historie. Git ist **verteilt**, das heißt: Jede lokale Kopie enthält grundsätzlich die vollständige Versionsgeschichte.

## Warum ist das so?
Ohne Versionsmanagement entstehen schnell Probleme:
- Änderungen überschreiben sich gegenseitig
- Fehler lassen sich nicht sauber zurückverfolgen
- Teamarbeit wird unübersichtlich
- Releases und Hotfixes sind schwer kontrollierbar

Git löst das, indem jede Änderung in nachvollziehbare Einheiten zerlegt wird.

## Zusammenspiel
- [[Debugging]] und Bugfixing werden sauber dokumentiert.
- [[Statische und dynamischen Testverfahren]] sowie [[Testvarianten (Unit-Tests, Integrationstests, Systemtests...)]] laufen häufig automatisiert bei Commits oder Pull Requests.
- [[Deploymentstrategien]] bauen oft direkt auf Branching, Tags und Releases auf.
- [[Automatisierung]] nutzt Git häufig als Auslöser für CI/CD-Pipelines.

## Eigene Worte (prüfungsnah)
Git ist wie eine lückenlose Projekthistorie mit Zeitmaschine. Ich kann sehen, wer was wann geändert hat, Änderungen in Paketen speichern, parallel in Branches arbeiten und später alles kontrolliert zusammenführen.

## Zentrale Begriffe
| Begriff | Erklärung | Prüfungsrelevanter Punkt |
|---|---|---|
| Repository | Projekt mit Historie | lokal oder remote |
| Working Tree | aktuelle lokale Dateien | hier wird gearbeitet |
| Staging Area | Vorbereitungsbereich für den nächsten Commit | mit `git add` befüllt |
| Commit | gespeicherter Änderungsstand | sollte fachlich zusammenhängend sein |
| Branch | Entwicklungszweig | trennt Features oder Fixes |
| Merge | Zusammenführen von Branches | kann Konflikte erzeugen |
| Pull | lädt Änderungen vom Remote | holt fremde Commits lokal |
| Push | überträgt lokale Commits zum Remote | veröffentlicht eigene Änderungen |
| Clone | vollständige Kopie eines Repositories | inkl. Historie |
| Tag | Markierung eines Versionsstands | oft für Releases |

## Typischer Arbeitsablauf
| Schritt | Git-Befehl | Zweck |
|---|---|---|
| Repository holen | `git clone` | Projekt lokal verfügbar machen |
| Änderungen prüfen | `git status` | Überblick über geänderte Dateien |
| Änderungen vormerken | `git add` | Inhalte für Commit auswählen |
| Version speichern | `git commit` | nachvollziehbaren Stand ablegen |
| Aktualisieren | `git pull` | Stand mit Remote abgleichen |
| Veröffentlichen | `git push` | Änderungen teilen |

## Branches und Zusammenarbeit
**Warum Branches?**
Weil mehrere Personen oder Themen parallel bearbeitet werden können, ohne den stabilen Hauptzweig direkt zu gefährden.

Typische Beispiele:
- Feature-Branch für neue Funktion
- Bugfix-Branch für Fehlerbehebung
- Release-Branch zur Auslieferung

**Merge-Konflikt:**
Wenn zwei Änderungen dieselbe Stelle betreffen, kann Git nicht automatisch entscheiden. Dann muss ein Mensch fachlich korrekt zusammenführen.

## Git im Prüfungszusammenhang
| Situation | Typische Erwartung |
|---|---|
| "Erklären Sie den Unterschied zwischen Git und GitHub" | Git = Werkzeug, GitHub = Hosting-Plattform |
| "Was macht `git add`?" | Dateien in die Staging Area übernehmen |
| "Warum Commits klein halten?" | Bessere Nachvollziehbarkeit und einfacheres Debugging |
| "Wozu Branches?" | Parallelentwicklung und risikoarme Änderungen |

## Beispielaufgabe mit Lösung
**Aufgabe:** Ein Entwickler ändert zwei Dateien. Eine davon gehört zu einem Bugfix, die andere zu einem neuen Feature. Warum sollte er beides nicht in einem Commit speichern?

**Lösung:**
Beides sollte getrennt committed werden, weil:
1. ein Commit fachlich zusammenhängend sein soll,
2. der Bugfix sonst später schwer isoliert rückgängig oder nachverfolgt werden kann,
3. Reviews und Fehlersuche mit kleinen Commits deutlich einfacher sind.

**Prüfungsnahe Formulierung:**
Ein Commit soll eine klar abgegrenzte Änderung dokumentieren. Gemischte Commits verschlechtern Nachvollziehbarkeit, Testbarkeit und Rückverfolgbarkeit.

## Beispielbefehle
```bash
git status
git add login.py
git commit -m "Fixe Grenzwertpruefung beim Login"
git pull
git push
```

## Typische Prüfungsszenarien
- Begriffe wie Repo, Commit, Branch und Merge erklären.
- Verteiltes Versionsmanagement von zentralem unterscheiden.
- Sinn der Staging Area beschreiben.
- Konfliktsituation im Team erklären.
- Git als Grundlage für automatisierte Tests und Deployments einordnen.

## Merksätze
- Git speichert keine "Datei-Endstände", sondern nachvollziehbare Änderungshistorie.
- Kleine, saubere Commits sind leichter testbar und reviewbar.
- Branches schaffen Sicherheit für parallele Arbeit.
