# On-Premises, Cloud, Housing, Hosting sowie IaaS, PaaS und SaaS

## Definition
Diese Begriffe beschreiben, **wo** IT betrieben wird und **wer** welche Verantwortung übernimmt.

Wichtige Modelle:
- **On-Premises**
- **Housing / Colocation**
- **Hosting**
- **IaaS**
- **PaaS**
- **SaaS**

## Warum ist das so?
Unternehmen müssen entscheiden:
- wo die Hardware steht
- wer Betrieb und Wartung übernimmt
- wie viel Kontrolle nötig ist
- wie flexibel und skalierbar die Lösung sein soll
- ob eher Investitionskosten oder laufende Kosten gewünscht sind

Je nach Modell verschiebt sich die Verantwortung zwischen Kunde und Anbieter.

## Zusammenspiel
- [[Virtualisierung (Bare-Metal, Hypervisor, Container)]] ist technische Basis vieler Cloud-Modelle.
- [[Server und Storage]] beschreibt die bereitgestellten Ressourcen.
- [[Deploymentstrategien]] werden je nach Betriebsmodell anders umgesetzt.
- [[2-Tier-, 3-Tier- und Multi-Tier-Architekturen]] laufen in allen Modellen, aber mit unterschiedlicher Verantwortung.

## Eigene Worte (prüfungsnah)
Der Kernunterschied liegt nicht nur im Ort der Server, sondern in der Verantwortung. Je weiter man von On-Premises Richtung SaaS geht, desto weniger betreibt man selbst und desto mehr übernimmt der Anbieter.

## Betriebsmodelle
| Modell | Wer besitzt die Hardware? | Wer betreibt was? |
|---|---|---|
| On-Premises | Unternehmen | fast alles selbst |
| Housing | Unternehmen | Hardware gehört dem Unternehmen, Standort/Umgebung liefert Anbieter |
| Hosting | Anbieter | Hardware beim Anbieter, OS/Software oft teilweise beim Kunden |

## Cloud-Service-Modelle
| Modell | Anbieter übernimmt | Kunde übernimmt |
|---|---|---|
| IaaS | Infrastruktur, Virtualisierung, Hardware | OS, Anwendungen, Daten |
| PaaS | Infrastruktur plus Laufzeitumgebung / Plattform | Anwendung, Daten |
| SaaS | komplette Anwendung | Nutzung, Konfiguration, Inhalte |

## Typische Beispiele
| Modell | Beispielhafte Vorstellung |
|---|---|
| On-Premises | eigener Serverraum im Unternehmen |
| Housing | eigener Server im fremden Rechenzentrum |
| Hosting | gemieteter dedizierter Server |
| IaaS | virtuelle Maschine in der Cloud |
| PaaS | bereitgestellte App-Plattform oder Datenbankplattform |
| SaaS | fertige Office- oder CRM-Anwendung im Browser |

## Vor- und Nachteile grob
| Modell | Vorteil | Nachteil |
|---|---|---|
| On-Premises | maximale Kontrolle | hoher Betriebsaufwand |
| Housing | professionelle Umgebung | eigene Hardware bleibt Verantwortung |
| Hosting | weniger Hardwareaufwand | weniger direkte Kontrolle |
| IaaS | flexibel, skalierbar | OS-Betrieb bleibt beim Kunden |
| PaaS | weniger Betriebsaufwand | geringere Plattformfreiheit |
| SaaS | sehr wenig Betriebsaufwand | geringste technische Kontrolle |

## Beispielaufgabe mit Lösung
**Aufgabe:** Ein Unternehmen möchte nur noch eine fertige Bürosoftware per Browser nutzen und sich weder um Server noch um Updates kümmern. Welches Modell passt am besten?

**Lösung:**
**SaaS**

**Begründung:**
1. Die Anwendung wird fertig bereitgestellt.
2. Der Anbieter übernimmt Betrieb und Updates.
3. Das Unternehmen nutzt die Software nur noch als Dienst.

## Typische Prüfungsszenarien
- On-Premises, Housing und Hosting unterscheiden.
- IaaS, PaaS und SaaS gegeneinander abgrenzen.
- Verantwortlichkeiten zwischen Kunde und Anbieter erklären.
- passende Modelle für konkrete Anforderungen auswählen.

## Merksätze
- On-Premises = viel Kontrolle, viel Verantwortung.
- SaaS = wenig technische Verantwortung, aber auch wenig Kontrolle.
- IaaS, PaaS und SaaS unterscheiden sich vor allem in der Betriebstiefe.
