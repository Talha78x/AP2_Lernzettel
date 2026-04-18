# Netzwerktopologien und Netzwerkpläne

## Definition
**Netzwerktopologien** beschreiben die physische oder logische Anordnung von Geräten und Verbindungen in einem Netzwerk. **Netzwerkpläne** dokumentieren diese Struktur grafisch und textlich.

## Warum ist das so?
Die Topologie beeinflusst direkt:
- Ausfallsicherheit
- Kosten
- Erweiterbarkeit
- Fehlersuche
- Leistungsfähigkeit

Ein gutes Netzwerk braucht deshalb nicht nur funktionierende Technik, sondern auch eine verständliche Struktur und saubere Dokumentation.

## Zusammenspiel
- [[LAN, WAN, WLAN ....]] beschreibt, in welchem Netzkontext eine Topologie eingesetzt wird.
- [[Strukturierte Verkabelung (Kupfer, Glasfaser, Funk, WLAN und Bluetooth)]] betrifft die physische Umsetzung.
- [[Spanning Tree]] ist wichtig in geschalteten Topologien mit Redundanz.
- [[VLAN (Arten, Trunking ...)]] wird in Netzwerkplänen oft gemeinsam mit Topologien dokumentiert.
- [[Routing (statisch, dynamisch, Inter-VLAN, Protokolle wie OSPF, RIP, BGP)]] ergänzt die logische Struktur zwischen Netzen.

## Eigene Worte (prüfungsnah)
Die Topologie ist der Bauplan des Netzes. Sie beschreibt, wer mit wem wie verbunden ist. Der Netzwerkplan ist die Dokumentation dazu, damit Aufbau, Adressierung, Geräte und Verbindungen nachvollziehbar bleiben.

## Wichtige Topologien
| Topologie | Aufbau | Vorteil | Nachteil |
|---|---|---|---|
| Stern | alle Geräte an zentralem Punkt | leicht erweiterbar, Fehler gut eingrenzbar | Zentrale Komponente kritisch |
| Bus | alle Geräte an gemeinsamer Leitung | geringer Verkabelungsaufwand | störanfällig, heute veraltet |
| Ring | jedes Gerät mit zwei Nachbarn | definierte Struktur | Unterbrechung kann kritisch sein |
| Mesh / Vermaschung | mehrere redundante Wege | hohe Ausfallsicherheit | hoher Aufwand |
| Baum | mehrere Sterne hierarchisch verbunden | gut skalierbar | Abhängigkeit von oberen Ebenen |

## Typische Praxisbewertung
| Topologie | Typischer Einsatz heute |
|---|---|
| Stern | Standard im LAN |
| Mesh | Router, WAN, Funknetze, Backbone |
| Baum | größere Unternehmensnetze |
| Bus | historisch |
| Ring | Spezialfälle oder historische Technologien |

## Netzwerkpläne: Was sollte hinein?
| Inhalt | Warum wichtig? |
|---|---|
| Geräte mit Namen und Typ | Übersicht und Inventarisierung |
| Verbindungen und Ports | Fehlersuche und Betrieb |
| IP-Adressen / Subnetze | Adressplanung und Routing |
| VLAN-Zuordnung | Segmentierung sichtbar machen |
| Router, Firewalls, Switches | Netzgrenzen und zentrale Komponenten erkennen |
| Internet- / WAN-Anbindung | Abhängigkeiten verstehen |

## Physisch vs. logisch
| Sicht | Frage |
|---|---|
| physische Topologie | Wie sind Geräte tatsächlich verkabelt oder verbunden? |
| logische Topologie | Wie fließen Daten und wie sind Netze/VLANs logisch getrennt? |

Ein Netz kann physisch sternförmig aufgebaut sein, aber logisch mehrere VLANs und Routing-Zonen enthalten.

## Beispielaufgabe mit Lösung
**Aufgabe:** In einem Büro sind alle PCs mit einem zentralen Switch verbunden. Welcher Topologietyp liegt vor und was ist der zentrale Nachteil?

**Lösung:**
- Topologie: **Stern**
- Nachteil: Der zentrale Switch ist ein kritischer Punkt. Fällt er aus, ist das gesamte angeschlossene Teilnetz betroffen.

## Typische Prüfungsszenarien
- Stern-, Bus-, Ring- und Mesh-Topologie unterscheiden.
- physische und logische Topologie abgrenzen.
- erklären, warum die Stern-Topologie heute Standard ist.
- Inhalte eines sauberen Netzwerkplans benennen.

## Merksätze
- Heute dominiert im LAN meist die Stern-Topologie.
- Redundanz erhöht Verfügbarkeit, aber auch Komplexität.
- Ein guter Netzwerkplan spart im Fehlerfall viel Zeit.
