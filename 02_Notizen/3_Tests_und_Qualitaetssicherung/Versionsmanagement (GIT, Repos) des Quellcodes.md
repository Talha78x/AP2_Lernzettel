# Versionsmanagement GIT, Repos des Quellcodes

**Versionsmanagementsysteme (VCS)** sind in der modernen IT unverzichtbar, um Änderungen an Quellcode, [[Skript- und Shellprogrammierung|Skripten]] oder Konfigurationsdateien ("Infrastructure as Code") nachvollziehbar zu speichern.

Das absolute Standard-Tool heute ist **Git** (ein verteiltes Versionsmanagementsystem). 

**Wichtige Begriffe für die IHK-Prüfung:**
- **Repository (Repo):** Die "Datenbank", in der das Projekt samt seiner gesamten Änderungshistorie liegt.
- **Working Copy / Working Tree:** Die lokalen Dateien auf dem PC des Entwicklers, an denen er gerade arbeitet.
- **Staging Area (Index):** Ein Zwischenbereich. Mit `git add` markiert man geänderte Dateien, die in den nächsten Versionsstand aufgenommen werden sollen.
- **Commit:** Speichert die Dateien aus der Staging Area fest als neue Version im lokalen Repository ab (meist mit einer Commit-Message, z.B. `git commit -m "Bugfix Login"`).
- **Push / Pull:** Überträgt lokale Commits auf einen zentralen Server (z. B. GitHub, GitLab) bzw. lädt Änderungen von dort herunter.
- **Branch:** Ein separater Entwicklungszweig. Man kann an neuen Features arbeiten, ohne den stabilen Hauptzweig (meist `main` oder `master`) zu zerstören.

Durch Git können ganze Teams gleichzeitig an denselben Dateien arbeiten. Kommt es zu Konflikten (zwei Personen haben dieselbe Zeile geändert), müssen diese beim *Merge* (Zusammenführen) aufgelöst werden.

Querverweise: [[Deploymentstrategien]], [[Automatisierung]].
