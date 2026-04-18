# Strukturierte Verkabelung (Kupfer, Glasfaser, Funk, WLAN und Bluetooth)

## Definition
Die **strukturierte Verkabelung** ist ein standardisierter Aufbau der Netzwerk-Infrastruktur in Gebäuden und auf Geländen. Sie sorgt dafür, dass Übertragungsmedien, Verteiler, Anschlussdosen und Leitungswege logisch geplant und langfristig nutzbar sind.

## Warum ist das so?
Ein Netzwerk soll:
- erweiterbar
- wartbar
- dokumentierbar
- störungsarm
- standardisiert

sein. Ohne strukturierte Verkabelung entstehen schnell chaotische Einzelverkabelungen, die teuer, fehleranfällig und schwer erweiterbar sind.

## Zusammenspiel
- [[LAN, WAN, WLAN ....]] beschreibt, in welchem Netztyp die Medien eingesetzt werden.
- [[Netzwerktopologien und Netzwerkpläne]] dokumentiert Aufbau und Anbindung.
- [[OSI und TCP-IP Modell]] ordnet Verkabelung primär auf Schicht 1 ein.
- [[Strukturierte Verkabelung (Kupfer, Glasfaser, Funk, WLAN und Bluetooth)]] bildet die physische Grundlage für Switches, VLANs, Routing und WLAN-Zellen.

## Eigene Worte (prüfungsnah)
Strukturierte Verkabelung ist der geordnete Grundriss der physischen Netzwerktechnik. Sie legt fest, wo welches Medium sinnvoll ist und wie Arbeitsplätze, Etagen und Gebäude sauber verbunden werden.

## Die drei Bereiche
| Bereich | Aufgabe | Typisches Medium |
|---|---|---|
| Primärbereich | Verbindung mehrerer Gebäude / Campus | meist Glasfaser |
| Sekundärbereich | Verbindung zwischen Gebäude- und Etagenverteilern | oft Glasfaser |
| Tertiärbereich | Verbindung vom Etagenverteiler zur Anschlussdose | meist Kupfer |

## Kupfer, Glasfaser und Funk im Vergleich
| Medium | Vorteile | Nachteile | Typischer Einsatz |
|---|---|---|---|
| Kupfer (Twisted Pair) | günstig, leicht zu installieren, RJ45 weit verbreitet | begrenzte Länge, störanfälliger als Glasfaser | Arbeitsplatz und Tertiärbereich |
| Glasfaser | hohe Reichweite, hohe Datenrate, unempfindlich gegen EM-Störungen | teurer, aufwendiger zu spleißen/anschließen | Backbone, Gebäude- und Standortanbindung |
| Funk / WLAN | mobil, keine Kabel bis zum Endgerät nötig | geteiltes Medium, störanfällig, Sicherheitsbedarf | mobile Clients |
| Bluetooth | sehr kurze Distanz, geringer Energiebedarf | geringe Reichweite und Datenrate | PAN, Headsets, Peripherie |

## Wichtige Praxisregeln
| Thema | Typische Aussage |
|---|---|
| Kupferlänge | im Ethernet meist maximal ca. 100 m pro Strecke |
| Glasfaser | ideal bei langen Strecken und Potentialunterschieden |
| WLAN | braucht saubere Ausleuchtung und Kanalkonzept |
| Bluetooth | kein Ersatz für klassisches LAN |

## Wann welches Medium?
| Situation | Sinnvolles Medium | Begründung |
|---|---|---|
| Arbeitsplatz im Büro | Kupfer | günstig und standardisiert |
| Verbindung zwischen zwei Etagenverteilern | Glasfaser | Reichweite und Störsicherheit |
| mobiles Tablet im Besprechungsraum | WLAN | Bewegungsfreiheit |
| Headset zur Telefonie | Bluetooth | kurze Distanz, wenig Energiebedarf |

## Prüfungsnahe Unterschiede
### Kupfer
- elektrisch
- kostengünstig
- typisch im Etagenbereich

### Glasfaser
- optisch
- große Reichweite
- hohe Datenrate
- unempfindlich gegen elektromagnetische Störungen

### WLAN
- Funknetz auf Basis von IEEE 802.11
- gemeinsames Übertragungsmedium
- stark von Planung, Kanalwahl und Umgebung abhängig

### Bluetooth
- Kurzstreckenfunk
- typisches PAN-Medium

## Beispielaufgabe mit Lösung
**Aufgabe:** Zwei Gebäude eines Unternehmens sollen mit hoher Bandbreite und störsicher verbunden werden. Welches Medium ist am besten geeignet?

**Lösung:**
**Glasfaser**

**Begründung:**
1. hohe Reichweite
2. hohe Übertragungsrate
3. unempfindlich gegenüber elektromagnetischen Störungen
4. typisch für Primär- oder Sekundärbereich

## Typische Prüfungsszenarien
- Primär-, Sekundär- und Tertiärbereich unterscheiden.
- Kupfer und Glasfaser vergleichen.
- maximale Kupferstrecke grob kennen.
- WLAN und Bluetooth korrekt abgrenzen.
- passende Medien für konkrete Einsatzfälle auswählen.

## Merksätze
- Kupfer für den Arbeitsplatz, Glasfaser für Backbone und längere Strecken.
- Strukturierte Verkabelung schafft Ordnung und Zukunftssicherheit.
- Funk ergänzt die Verkabelung, ersetzt sie aber nicht überall.
