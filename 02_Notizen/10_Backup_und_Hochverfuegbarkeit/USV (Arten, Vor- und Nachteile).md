# USV (Arten, Vor- und Nachteile)

## Definition
Eine **USV (Unterbrechungsfreie Stromversorgung)** schützt IT-Systeme bei Stromausfall, Unterspannung, Überspannung oder anderen Störungen der Stromversorgung. Sie dient vor allem dem Schutzziel **Verfügbarkeit**.

## Warum ist das so?
Stromprobleme können große Schäden auslösen:
- abrupter Serverausfall
- Datenverlust
- Dateisystemfehler
- Hardwareprobleme

Eine USV überbrückt kurze Ausfälle oder schafft Zeit für geregeltes Herunterfahren.

## Zusammenspiel
- [[Server und Storage]] beschreibt typische Schutzobjekte.
- [[Notfallkonzept, Disaster Recovery]] berücksichtigt Stromausfälle als Störfall.
- [[Schutzziele der IT]] ordnet die USV primär der Verfügbarkeit zu.
- [[USV (Arten, Vor- und Nachteile)]] ergänzt andere Verfügbarkeitsmaßnahmen wie Cluster oder Backups, ersetzt diese aber nicht.

## Eigene Worte (prüfungsnah)
Eine USV ist kein Stromgenerator für ewigen Betrieb, sondern eine Schutz- und Überbrückungslösung. Sie hält Systeme kurz am Leben oder sorgt für ein sauberes Herunterfahren.

## Hauptarten
| Typ | Alternative Bezeichnung | Merkmal |
|---|---|---|
| VFD | Offline / Standby | einfache Grundabsicherung |
| VI | Line-Interactive | gleicht Spannungsschwankungen besser aus |
| VFI | Online / Doppelwandler | höchste Qualität, 0 ms Umschaltzeit |

## Vergleich
| Typ | Vorteil | Nachteil | Typischer Einsatz |
|---|---|---|---|
| VFD | günstig, effizient | wenig Schutz, Umschaltzeit | Arbeitsplatz, kleine Geräte |
| VI | besser bei Spannungsschwankungen | nicht so vollständig wie Online-USV | kleine Serverräume |
| VFI | beste Stromqualität | teuer, höherer Energiebedarf | Rechenzentrum, kritische Systeme |

## Typische Prüfungslogik
| Anforderung | passende USV |
|---|---|
| einfacher PC-Arbeitsplatz | VFD |
| kleiner Serverschrank | VI |
| hochkritische Server im RZ | VFI |

## Beispielaufgabe mit Lösung
**Aufgabe:** Für einen besonders kritischen Datenbankserver wird eine USV mit möglichst perfekter Stromqualität und ohne Umschaltzeit benötigt. Welcher Typ passt?

**Lösung:**
**VFI / Online-USV / Doppelwandler**

**Begründung:**
Dieser Typ versorgt das System permanent über den Wandler und bietet deshalb 0 ms Umschaltzeit sowie sehr hohe Stromqualität.

## Typische Prüfungsszenarien
- VFD, VI und VFI unterscheiden.
- erklären, warum eine USV Verfügbarkeit unterstützt.
- USV von Notstromaggregat abgrenzen.
- passenden Typ für ein Einsatzszenario auswählen.

## Merksätze
- USV schützt vor Stromproblemen, nicht vor allen Ausfällen.
- VFI ist die stärkste, aber teuerste Lösung.
- Eine USV schafft Zeit, keine unbegrenzte Laufzeit.
