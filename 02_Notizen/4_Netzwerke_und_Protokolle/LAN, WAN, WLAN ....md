# LAN, WAN, WLAN ....

## Definition
Netzwerke lassen sich nach Reichweite, Trägermedium und Einsatzgebiet unterscheiden.

Wichtige Begriffe sind:
- **LAN (Local Area Network)**: lokales Netzwerk in Gebäude, Etage oder Campus
- **WLAN (Wireless LAN)**: drahtlose Form eines LAN
- **WAN (Wide Area Network)**: standortübergreifendes Netz über größere Entfernungen
- zusätzlich oft **MAN** und **PAN**

## Warum ist das so?
Nicht jedes Netz hat dieselben Anforderungen:
- Ein Büro braucht hohe Geschwindigkeit und geringe Latenz.
- Eine Standortvernetzung braucht Reichweite und Provider-Anbindung.
- Funknetze brauchen Mobilität, aber auch mehr Schutz gegen Störungen und Mithören.

Darum unterscheidet man Netzarten nicht nur geografisch, sondern auch technisch und organisatorisch.

## Zusammenspiel
- [[Strukturierte Verkabelung (Kupfer, Glasfaser, Funk, WLAN und Bluetooth)]] beschreibt die Übertragungsmedien.
- [[VPN (Tunneling, standortübergreifende Kommunikation)]] wird oft über WAN-Verbindungen genutzt.
- [[Netzwerktopologien und Netzwerkpläne]] beschreibt den strukturellen Aufbau solcher Netze.
- [[Anforderungen an Bandbreite, Latenz, Verfügbarkeit, Übertragungsmedien und Netzwerksicherheit]] passt fachlich direkt dazu.
- [[Standardprotokolle (TCP, UDP, MAC, ARP, ICMP, HTTP, HTTPS, FTP, SMTP...)]] laufen in allen Netzarten, aber unter unterschiedlichen Rahmenbedingungen.

## Eigene Worte (prüfungsnah)
LAN, WLAN und WAN beschreiben nicht einfach nur "mit Kabel" oder "ohne Kabel", sondern vor allem Reichweite, Verantwortung und technische Eigenschaften. Ein WLAN ist kein eigenes Gegenstück zum LAN, sondern meist die drahtlose Zugangsform zu einem lokalen Netz.

## Gegenüberstellung
| Netztyp | Reichweite | Typische Technik | Typische Eigenschaft |
|---|---|---|---|
| LAN | lokal | Ethernet, Switches | hohe Datenrate, geringe Latenz |
| WLAN | lokal | IEEE 802.11 | mobil, aber störanfälliger |
| WAN | großräumig | Provider-Strecken, MPLS, Internet | höhere Latenzen, geringere Kontrolle |
| MAN | stadtweit | Glasfaser, Provider-Netz | verbindet mehrere Standorte in einer Region |
| PAN | sehr klein | Bluetooth, NFC | Geräte im persönlichen Umfeld |

## LAN
Typische Merkmale:
- hohe Übertragungsgeschwindigkeit
- eigene Kontrolle durch das Unternehmen
- meist strukturierte Verkabelung und Switch-Infrastruktur

## WLAN
Typische Merkmale:
- flexible Endgeräteanbindung ohne Kabel
- gemeinsame Nutzung des Funkmediums
- Reichweite abhängig von Hindernissen, Kanalbelegung und Sendeleistung
- Sicherheitsbedarf durch Verschlüsselung und Authentifizierung

**Wichtig:** WLAN ist komfortabel, aber nicht automatisch langsamer oder unsicherer "per Definition". Die Qualität hängt stark von Planung, Funkumgebung und Konfiguration ab.

## WAN
Typische Merkmale:
- verbindet entfernte Standorte
- oft über Provider oder Internet realisiert
- höhere Latenz als im LAN
- häufige Kombination mit VPN

## Beispielaufgabe mit Lösung
**Aufgabe:** Ordne zu:
1. Netzwerk innerhalb eines Bürogebäudes
2. Funkanbindung von Notebooks im Besprechungsraum
3. Verbindung zwischen Berlin und München über einen Provider

**Lösung:**
1. **LAN**
2. **WLAN**
3. **WAN**

**Prüfungsbegründung:**
Entscheidend sind Reichweite, Übertragungsmedium und organisatorische Einbindung.

## Typische Prüfungsszenarien
- LAN, WLAN und WAN gegeneinander abgrenzen.
- MAN und PAN korrekt einordnen.
- erklären, warum WAN-Verbindungen meist höhere Latenzen haben.
- WLAN als drahtlose Zugangstechnik zum LAN beschreiben.

## Merksätze
- WLAN ist meist Teil eines LAN, nicht dessen Ersatzbegriff.
- WAN bedeutet große Distanz und oft Provider-Abhängigkeit.
- Mit wachsender Reichweite steigen meist Latenz und organisatorische Komplexität.
