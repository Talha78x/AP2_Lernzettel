# Deploymentstrategien

## Definition
**Deployment** bezeichnet die Bereitstellung, Verteilung oder Aktualisierung von Software, Diensten oder ganzen Systemständen in Test-, Staging- oder Produktivumgebungen.

## Warum ist das so?
Softwareänderungen bringen immer Risiko mit:
- Fehler im Rollout
- Ausfälle im Betrieb
- Inkompatibilitäten
- Nutzerstörungen

Darum braucht man Strategien, die Updates kontrolliert, reproduzierbar und möglichst risikoarm in den Betrieb bringen.

## Zusammenspiel
- [[2-Tier-, 3-Tier- und Multi-Tier-Architekturen]] bestimmt, welche Schichten deployt werden müssen.
- [[Virtualisierung (Bare-Metal, Hypervisor, Container)]] erleichtert oft standardisierte Rollouts.
- [[On-Premises, Cloud, Housing, Hosting sowie IaaS, PaaS und SaaS]] beeinflusst, wie Deployments technisch umgesetzt werden.
- [[Load Balancing]] ist bei Blue/Green oder Canary oft direkt beteiligt.
- [[Versionsmanagement (GIT, Repos) des Quellcodes]] dokumentiert Änderungen und bildet oft die Pipeline-Basis.

## Eigene Worte (prüfungsnah)
Deployment ist nicht einfach "Installation". Es ist der geplante Weg, neue Softwarestände kontrolliert in Betrieb zu bringen, ohne unnötige Ausfälle oder Überraschungen zu erzeugen.

## Klassische Rollout-Strategien
| Strategie | Beschreibung | Vorteil | Nachteil |
|---|---|---|---|
| Big Bang | alle Nutzer/Systeme gleichzeitig umstellen | schneller Wechsel | hohes Risiko |
| phasenweise / iterativ | schrittweise Einführung | Fehler betreffen kleinere Gruppen | längere Parallelphase |

## Moderne Deployment-Strategien
| Strategie | Funktionsweise | Typischer Vorteil |
|---|---|---|
| Blue/Green | zwei Produktivumgebungen, Umschaltung auf neue Umgebung | schnelles Zurückschalten möglich |
| Canary | kleine Nutzergruppe erhält neues Release zuerst | Risiken früh erkennbar |
| Rolling Update | Instanzen nacheinander ersetzen | weniger harter Cut |

## Typische Auswahlkriterien
| Frage | Bedeutung |
|---|---|
| Wie kritisch ist der Dienst? | bestimmt Risikoakzeptanz |
| Wie leicht kann man zurückrollen? | wichtig bei Fehlern |
| Gibt es mehrere Instanzen? | relevant für Rolling oder Blue/Green |
| Wie viele Nutzer sind betroffen? | beeinflusst Pilot-/Canary-Ansatz |

## Beispielaufgabe mit Lösung
**Aufgabe:** Eine neue Webanwendung soll zuerst nur für 5 % der Nutzer freigeschaltet werden, um Probleme früh zu erkennen. Welche Strategie passt?

**Lösung:**
**Canary Deployment**

**Begründung:**
1. Nur ein kleiner Teil der Nutzer erhält die neue Version.
2. Probleme werden früh sichtbar.
3. Das Risiko für alle Nutzer ist geringer.

## Typische Prüfungsszenarien
- Big Bang und phasenweisen Rollout vergleichen.
- Blue/Green und Canary unterscheiden.
- erklären, warum Rückfallmöglichkeiten wichtig sind.
- Deployment von Installation oder Entwicklung abgrenzen.

## Merksätze
- Deployment ist kontrollierte Bereitstellung, nicht nur Kopieren von Dateien.
- Je kritischer der Dienst, desto wichtiger sind Risiko- und Rollback-Strategien.
- Canary testet klein, Blue/Green schaltet um.
