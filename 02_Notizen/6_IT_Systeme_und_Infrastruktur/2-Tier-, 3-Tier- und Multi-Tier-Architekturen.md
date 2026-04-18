# 2-Tier-, 3-Tier- und Multi-Tier-Architekturen

## Definition
**Tier-Architekturen** beschreiben, wie die Aufgaben einer Anwendung auf verschiedene Schichten oder Systeme verteilt werden. Typische Aufgaben sind:
- **Präsentation** (Benutzeroberfläche)
- **Geschäftslogik**
- **Datenhaltung**

Je nach Architektur liegen diese Aufgaben auf zwei, drei oder mehr Ebenen.

## Warum ist das so?
Wenn alle Aufgaben in einer einzigen Anwendung oder auf einem einzigen System liegen, entstehen schnell Probleme:
- schlechte Skalierbarkeit
- schwierige Wartung
- hohe Abhängigkeit zwischen Oberfläche, Logik und Daten
- geringere Sicherheit

Durch die Aufteilung in Schichten lassen sich Systeme besser pflegen, absichern und erweitern.

## Zusammenspiel
- [[Betriebssysteme und Anwendungen]] liefert die Plattform für die einzelnen Schichten.
- [[Server und Storage]] zeigt, auf welchen Systemen die Tiers laufen können.
- [[On-Premises, Cloud, Housing, Hosting sowie IaaS, PaaS und SaaS]] beschreibt, wo diese Tiers betrieben werden.
- [[Load Balancing]] ist vor allem bei der Logik- oder Webschicht relevant.
- [[Deploymentstrategien]] greifen direkt in die Verteilung und Aktualisierung der Tiers ein.

## Eigene Worte (prüfungsnah)
Eine Tier-Architektur teilt eine Anwendung in sinnvolle Aufgabenbereiche auf. Die Oberfläche spricht nicht direkt alles selbst ab, sondern ruft oft eine separate Logikschicht auf, die wiederum mit der Datenbank kommuniziert.

## 2-Tier-Architektur
| Schicht | Aufgabe |
|---|---|
| Client | Oberfläche und oft ein Teil der Logik |
| Server | Datenhaltung, oft Datenbank |

**Typischer Fall:**
Ein Fat Client greift direkt auf einen Datenbankserver zu.

**Nachteile:**
- Logik oft auf vielen Clients verteilt
- Updates aufwendiger
- direkte Datenbankzugriffe durch Clients sind sicherheits- und wartungsintensiver

## 3-Tier-Architektur
| Schicht | Aufgabe |
|---|---|
| Presentation Tier | Benutzeroberfläche, z. B. Browser |
| Application Tier | Geschäftslogik |
| Data Tier | Datenbank / Datenspeicher |

**Vorteile:**
- bessere Wartbarkeit
- bessere Skalierung
- bessere Trennung von Zuständigkeiten
- Datenbank direkter vom Benutzer getrennt

## Multi-Tier
Bei **Multi-Tier** wird weiter aufgeteilt, zum Beispiel:
- Webserver separat
- API separat
- Authentifizierungsdienst separat
- Cache separat
- Datenbank separat

Das ist besonders in größeren Web- und Cloud-Architekturen üblich.

## Vergleich
| Architektur | Vorteil | Nachteil | Typischer Einsatz |
|---|---|---|---|
| 2-Tier | einfach | schlechter skalierbar | kleine klassische Client-Server-Systeme |
| 3-Tier | gut wartbar, Standard | mehr Komponenten | Webanwendungen, Unternehmenssoftware |
| Multi-Tier | sehr flexibel und skalierbar | hohe Komplexität | große verteilte Systeme |

## Beispielaufgabe mit Lösung
**Aufgabe:** Ein Webbrowser greift auf einen Webserver zu. Dieser verarbeitet die Geschäftslogik und speichert Daten in einer separaten Datenbank. Welche Architektur liegt vor?

**Lösung:**
Eine **3-Tier-Architektur**.

**Begründung:**
1. Browser = Präsentationsschicht
2. Web-/Applikationsserver = Logikschicht
3. Datenbankserver = Datenschicht

## Typische Prüfungsszenarien
- 2-Tier und 3-Tier unterscheiden.
- Fat Client und Thin Client einordnen.
- Vorteile getrennter Logik- und Datenschicht erklären.
- Multi-Tier als Weiterentwicklung großer Systeme begründen.

## Merksätze
- Je mehr Tiers, desto besser trennbar, aber desto komplexer.
- 3-Tier ist der klassische Standard moderner Unternehmensanwendungen.
- Direkter Client-auf-Datenbank-Zugriff ist typisch für 2-Tier.
