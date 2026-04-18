# Snap-Shot, Versionierung, Hochverfügbarkeit (Clustering, Load Balancing, FHRP)

## Definition
Diese Begriffe beschreiben unterschiedliche Verfahren zur schnellen Wiederherstellung oder hohen Verfügbarkeit:
- **Snapshot**
- **Versionierung**
- **Clustering**
- **Load Balancing**
- **FHRP**

## Warum ist das so?
Nicht jeder Ausfall wird mit demselben Mittel behandelt:
- Ein Snapshot hilft beim schnellen Zurückrollen.
- Versionierung hilft bei alten Dateiständen.
- Clustering und Load Balancing halten Dienste verfügbar.
- FHRP schützt das Gateway auf Netzwerkebene.

Deshalb muss man diese Konzepte sauber voneinander trennen.

## Zusammenspiel
- [[Backupstrategien (Vollbackup, inkrementell, differentiell, kontinuierlich)]] bleibt für echte Datensicherung notwendig.
- [[Load Balancing]] und [[First-Hop Redundancy Protocol (FHRP)]] werden hier im HA-Kontext wieder aufgegriffen.
- [[Virtualisierung (Bare-Metal, Hypervisor, Container)]] nutzt Snapshots oft vor Änderungen.
- [[Notfallkonzept, Disaster Recovery]] ordnet diese Verfahren nach Wiederanlauf und Verfügbarkeit ein.

## Eigene Worte (prüfungsnah)
Snapshots, Versionierung und Hochverfügbarkeitsverfahren helfen auf unterschiedliche Weise, Ausfälle oder Fehler abzufangen. Die häufigste Prüfungsfalle ist, einen Snapshot mit einem echten Backup gleichzusetzen.

## Snapshot und Versionierung
| Begriff | Zweck | Grenze |
|---|---|---|
| Snapshot | Zustand zu einem Zeitpunkt einfrieren | kein vollwertiges Backup |
| Versionierung | ältere Stände von Dateien erhalten | schützt nicht automatisch gegen alle Ausfälle |

## Hochverfügbarkeit
| Begriff | Idee |
|---|---|
| Clustering | mehrere Server arbeiten als Verbund |
| Active/Active | mehrere Knoten arbeiten gleichzeitig |
| Active/Passive | ein Knoten aktiv, anderer wartet auf Ausfall |
| Load Balancing | verteilt Last auf mehrere Systeme |
| FHRP | sichert Default Gateway ab |

## Typische Abgrenzungen
| Begriff | schützt / hilft wobei? |
|---|---|
| Snapshot | schneller Rücksprung auf alten Zustand |
| Versionierung | ältere Datei- oder Dokumentstände |
| Cluster | Dienstverfügbarkeit bei Knotenausfall |
| Load Balancer | Lastverteilung und teilweise Ausfallsicherheit |
| FHRP | Gateway-Ausfallsicherheit |

## Beispielaufgabe mit Lösung
**Aufgabe:** Vor einem Update einer virtuellen Maschine soll der aktuelle Zustand schnell zurücksetzbar sein. Welche Technik ist dafür besonders passend?

**Lösung:**
**Snapshot**

**Begründung:**
Ein Snapshot friert den Zustand eines Systems oder Datenträgers zu einem definierten Zeitpunkt ein und erlaubt schnelles Rollback.

## Typische Prüfungsszenarien
- Snapshot und Backup unterscheiden.
- Active/Active und Active/Passive vergleichen.
- FHRP von Load Balancing abgrenzen.
- Versionierung für Dateiwiederherstellung einordnen.

## Merksätze
- Snapshot ist praktisch, aber kein Backup-Ersatz.
- Hochverfügbarkeit verhindert Ausfallfolgen, ersetzt aber keine Datensicherung.
- FHRP schützt das Gateway, nicht den ganzen Dienst.
