# Spanning Tree

## Definition
Das **Spanning Tree Protocol (STP)** verhindert **Schleifen (Loops)** in vermaschten Layer-2-Netzen. Es sorgt dafür, dass trotz redundanter Verbindungen nur ein schleifenfreier aktiver Pfad genutzt wird.

## Warum ist das so?
Auf Schicht 2 besitzen Ethernet-Frames keine eingebaute "Lebensdauer" wie die TTL bei IP. Wenn in einem Switch-Netz eine Schleife entsteht, können Broadcasts und unbekannte Unicasts endlos kreisen.

Das führt zu:
- **Broadcast Storms**
- vervielfachten Frames
- instabilen MAC-Tabellen
- massiven Netzstörungen

Redundante Verbindungen sind für Ausfallsicherheit wichtig, aber ohne STP wären sie gefährlich.

## Zusammenspiel
- [[OSI und TCP-IP Modell]] ordnet STP auf Schicht 2 ein.
- [[VLAN (Arten, Trunking ...)]] läuft oft gemeinsam mit STP in Switch-Infrastrukturen.
- [[Netzwerktopologien und Netzwerkpläne]] zeigt, warum vermaschte oder redundante Topologien STP brauchen.
- [[First-Hop Redundancy Protocol (FHRP)]] sichert Gateways ab, während STP Layer-2-Schleifen vermeidet.

## Eigene Worte (prüfungsnah)
STP ist die Sicherheitsbremse für redundante Switch-Verbindungen. Es erlaubt Reservepfade, verhindert aber, dass mehrere Layer-2-Wege gleichzeitig eine Schleife bilden.

## Grundprinzip
1. Switches tauschen **BPDUs** aus.
2. Es wird eine **Root Bridge** bestimmt.
3. Jeder Switch berechnet den besten Pfad zur Root Bridge.
4. Redundante Pfade werden logisch blockiert.
5. Fällt ein aktiver Pfad aus, kann ein blockierter Pfad freigeschaltet werden.

## Wichtige Begriffe
| Begriff | Bedeutung |
|---|---|
| BPDU | Steuerinformation für STP |
| Root Bridge | zentral gewählter Referenz-Switch |
| Root Port | bester Pfad eines Switches zur Root Bridge |
| Designated Port | aktiver Port eines Segments |
| Blocking Port | redundanter, vorerst gesperrter Port |

## STP, RSTP, MSTP
| Variante | Besonderheit |
|---|---|
| STP | klassischer Standard, eher langsam |
| RSTP | Rapid Spanning Tree, schnellere Umschaltung |
| MSTP | mehrere Instanzen, sinnvoll bei mehreren VLAN-Konzepten |

## Warum ist STP trotz Redundanz sinnvoll?
Redundanz bedeutet nicht, dass alle Wege gleichzeitig aktiv sein dürfen. Auf Layer 2 würde das ohne Kontrolle zu Schleifen führen. STP erlaubt daher Redundanz **mit kontrollierter Aktivierung**.

## Beispielaufgabe mit Lösung
**Aufgabe:** Zwei Switches sind über zwei Kabel miteinander verbunden. Kurz danach ist das Netz extrem langsam, Broadcasts nehmen stark zu. Welches Protokoll fehlt oder ist fehlerhaft?

**Lösung:**
Wahrscheinlich fehlt **STP** oder es arbeitet nicht korrekt.

**Begründung:**
1. Zwei parallele Layer-2-Wege erzeugen ohne Steuerung eine Schleife.
2. Broadcasts können sich vervielfachen.
3. STP würde einen redundanten Pfad blockieren und so den Loop verhindern.

## Typische Prüfungsszenarien
- erklären, warum Loops in Switch-Netzen gefährlich sind.
- Root Bridge und blockierte Ports beschreiben.
- STP von Routing unterscheiden.
- STP und RSTP grob abgrenzen.

## Merksätze
- Redundanz auf Layer 2 braucht Schleifenschutz.
- STP blockiert Reservepfade logisch, nicht physisch.
- Ohne STP können Broadcast Storms ein LAN sehr schnell lahmlegen.
