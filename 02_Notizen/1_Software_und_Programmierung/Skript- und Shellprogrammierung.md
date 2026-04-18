# Skript- und Shellprogrammierung

## Definition
Skripte sind ausführbare Textdateien zur Automatisierung von System- und Verwaltungsaufgaben (z. B. Bash, PowerShell, Python).

## Warum ist das so?
Administrationsaufgaben sind wiederkehrend (Logs, Backups, Benutzerverwaltung) und sollten reproduzierbar laufen.

## Zusammenspiel
- Basis für [[Automatisierung]].
- Nutzt Kontrollstrukturen aus [[Algorithmen und Kontrollstrukturen]].

## Beispiel (Bash)
```bash
#!/usr/bin/env bash
for f in *.log; do
  gzip "$f"
done
```

## Prüfungsszenario
**Aufgabe:** 500 Logdateien sollen komprimiert werden.

**Lösungsidee:** Schleife über Dateimenge, Fehlerbehandlung (existiert Datei?), Logging von Erfolgen/Fehlern.
