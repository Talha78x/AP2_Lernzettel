# Betriebssysteme und Anwendungen

## Definition
Ein **Betriebssystem (Operating System, OS)** verwaltet die Hardware-Ressourcen eines Systems und stellt grundlegende Dienste für Anwendungen bereit. Es bildet die Vermittlung zwischen Hardware und Software.

## Warum ist das so?
Programme sollen nicht direkt jede Hardware selbst steuern müssen. Das Betriebssystem übernimmt deshalb zentrale Aufgaben:
- Prozessverwaltung
- Speicherverwaltung
- Dateiverwaltung
- Benutzer- und Rechteverwaltung
- Geräte- und Treibersteuerung

Erst dadurch können Anwendungen standardisiert auf Systemressourcen zugreifen.

## Zusammenspiel
- [[Server und Storage]] zeigt typische Plattformen, auf denen Betriebssysteme laufen.
- [[Virtualisierung (Bare-Metal, Hypervisor, Container)]] trennt Betriebssysteme von physischer Hardware.
- [[Deploymentstrategien]] regelt die Verteilung von Betriebssystemen und Anwendungen.
- [[2-Tier-, 3-Tier- und Multi-Tier-Architekturen]] baut Anwendungen strukturell auf dem OS auf.

## Eigene Worte (prüfungsnah)
Das Betriebssystem ist die Grundschicht eines IT-Systems. Es sorgt dafür, dass CPU, RAM, Speicher und Geräte geordnet genutzt werden können. Anwendungen setzen darauf auf und nutzen die vom OS bereitgestellten Dienste.

## Wichtige Aufgaben des Betriebssystems
| Aufgabe | Bedeutung |
|---|---|
| Prozessverwaltung | steuert laufende Programme |
| Speicherverwaltung | verteilt RAM sinnvoll |
| Dateisystem | organisiert Dateien und Ordner |
| Benutzer-/Rechteverwaltung | schützt Daten und Funktionen |
| Geräteverwaltung | steuert Hardware über Treiber |

## Wichtige Eigenschaften
| Begriff | Bedeutung |
|---|---|
| Multi-User | mehrere Benutzer können das System nutzen |
| Multitasking | mehrere Programme laufen scheinbar gleichzeitig |
| präemptiv | das OS entzieht Prozessen CPU-Zeit kontrolliert |
| Echtzeitsystem | reagiert innerhalb definierter Zeitgrenzen |

## Anwendungen
Anwendungen nutzen Betriebssystemdienste, zum Beispiel:
- Office-Programme
- Webserver
- Datenbankdienste
- ERP-Systeme
- Fachanwendungen

In Unternehmen werden Anwendungen oft automatisiert installiert, verteilt und aktualisiert.

## Betriebssystem und Anwendung unterscheiden
| Ebene | Beispiel |
|---|---|
| Betriebssystem | Windows Server, Linux, macOS |
| Anwendung | Browser, Datenbank, ERP, Mailserver |

## Beispielaufgabe mit Lösung
**Aufgabe:** Warum ist ein Betriebssystem notwendig, damit eine Anwendung sinnvoll auf einem Rechner laufen kann?

**Lösung:**
Weil das Betriebssystem die Hardware verwaltet und standardisierte Dienste bereitstellt.

**Begründung:**
1. Anwendungen brauchen CPU-Zeit, Speicher und Dateizugriff.
2. Das OS koordiniert diese Ressourcen.
3. Ohne Betriebssystem müsste jede Anwendung Hardware direkt selbst ansteuern.

## Typische Prüfungsszenarien
- Betriebssystem und Anwendung abgrenzen.
- Multi-User, Multitasking und Echtzeit erklären.
- Aufgaben eines Betriebssystems aufzählen.
- erklären, warum Anwendungen auf OS-Diensten aufbauen.

## Merksätze
- Das Betriebssystem verwaltet Ressourcen, Anwendungen nutzen sie.
- Multitasking heißt geordnete Parallelität, nicht echte Gleichzeitigkeit auf jedem System.
- Ohne OS keine saubere Abstraktion zwischen Hardware und Software.
