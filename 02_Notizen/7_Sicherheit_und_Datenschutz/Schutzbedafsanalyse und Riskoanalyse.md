# Schutzbedafsanalyse und Riskoanalyse

## Definition
Die **Schutzbedarfsanalyse** bewertet, wie schwerwiegend die Folgen wären, wenn Schutzziele verletzt werden. Die **Risikoanalyse** untersucht zusätzlich konkrete Gefährdungen, Wahrscheinlichkeiten und Schäden.

## Warum ist das so?
Nicht jedes System ist gleich kritisch. Ein Testsystem für Schulungszwecke braucht andere Schutzmaßnahmen als:
- ein Produktionsserver
- ein Domaincontroller
- eine medizinische Anwendung
- ein Gehaltsabrechnungssystem

Sicherheit muss deshalb am tatsächlichen Risiko ausgerichtet werden und nicht pauschal für alles gleich aussehen.

## Zusammenspiel
- [[Schutzziele der IT]] liefert die Bewertungsgrundlage.
- [[DSGVO und IT-Grundschutz (Personbezogene Daten usw..)]] gibt besonders bei personenbezogenen Daten zusätzliche Bedeutung.
- [[TOM]] setzt Maßnahmen auf Basis von Schutzbedarf und Risiko um.
- [[Security by Design]] berücksichtigt diese Bewertung schon im Entwurf.

## Eigene Worte (prüfungsnah)
Die Schutzbedarfsanalyse fragt zuerst: "Wie schlimm wäre ein Schaden?" Die Risikoanalyse fragt danach: "Welche Gefahr droht konkret, wie wahrscheinlich ist sie und welche Maßnahmen sind nötig?"

## Schutzbedarfsanalyse
Typisch wird nach den Schutzzielen bewertet:
- **Vertraulichkeit**
- **Integrität**
- **Verfügbarkeit**

| Einstufung | Bedeutung |
|---|---|
| normal | begrenzte Auswirkungen |
| hoch | erhebliche Auswirkungen |
| sehr hoch | existenzbedrohend, gesetzlich kritisch oder mit schweren Folgen |

## Maximumprinzip
Wenn ein System bei einem Schutzziel besonders kritisch ist, bestimmt dieser höchste Wert oft den gesamten Schutzbedarf.

**Beispiel:**
- Vertraulichkeit: sehr hoch
- Integrität: hoch
- Verfügbarkeit: normal

=> Gesamtbewertung häufig: **sehr hoch**

## Risikoanalyse
Die Risikoanalyse betrachtet typischerweise:
- Gefährdung / Bedrohung
- Eintrittswahrscheinlichkeit
- Schadenshöhe
- daraus abgeleitetes Risiko

| Faktor | Frage |
|---|---|
| Bedrohung | Was kann passieren? |
| Wahrscheinlichkeit | Wie wahrscheinlich ist das? |
| Schaden | Wie schwer wären die Folgen? |
| Maßnahme | Was reduziert Risiko oder Schaden? |

## Schutzbedarf vs. Risiko
| Begriff | Fokus |
|---|---|
| Schutzbedarf | Bedeutung des Systems / Schadensausmaß |
| Risiko | Kombination aus Gefährdung, Wahrscheinlichkeit und Schaden |

## Beispielaufgabe mit Lösung
**Aufgabe:** Ein Server speichert Gesundheitsdaten. Für Vertraulichkeit ist die Einstufung "sehr hoch", für Integrität "hoch" und für Verfügbarkeit "normal". Welcher Schutzbedarf ist insgesamt anzusetzen?

**Lösung:**
**Sehr hoch**

**Begründung:**
Nach dem Maximumprinzip bestimmt die höchste Einzelbewertung den Gesamtschutzbedarf.

## Typische Prüfungsszenarien
- Schutzbedarf und Risiko unterscheiden.
- Maximumprinzip erklären.
- Vertraulichkeit, Integrität und Verfügbarkeit als Bewertungsmaßstab anwenden.
- aus einer Gefährdung sinnvolle Maßnahmen ableiten.

## Merksätze
- Schutzbedarf bewertet die Bedeutung, Risiko bewertet die Gefahrensituation.
- Hoher Schutzbedarf bedeutet meist strengere Maßnahmen.
- Das Maximumprinzip ist eine klassische Prüfungsfalle.
