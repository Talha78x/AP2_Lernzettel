# IPv6 (Grundlagen & Subnetting usw..)

## Definition
**IPv6** ist der Nachfolger von IPv4 und verwendet **128 Bit** lange Adressen. Die Schreibweise erfolgt hexadezimal in acht Blöcken zu je 16 Bit, zum Beispiel:

`2001:0db8:0000:0000:02aa:00ff:fe9a:4ca2`

Abkürzungen sind erlaubt:
- führende Nullen in einem Block dürfen weggelassen werden
- eine zusammenhängende Nullfolge darf einmalig mit `::` abgekürzt werden

Beispiel:
`2001:db8::2aa:ff:fe9a:4ca2`

## Warum ist das so?
IPv4-Adressen sind knapp. Zusätzlich soll IPv6 moderne Netzwerke verbessern:
- viel größerer Adressraum
- einfachere hierarchische Adressvergabe
- weniger Bedarf für NAT
- automatische Adresskonfiguration möglich
- effizientere Multicast-/Neighbor-Mechanismen

## Zusammenspiel
- [[OSI und TCP-IP Modell]] ordnet IPv6 auf Schicht 3 ein.
- [[Standardprotokolle (TCP, UDP, MAC, ARP, ICMP, HTTP, HTTPS, FTP, SMTP...)]] nutzt IPv6 wie IPv4 als Netzprotokoll.
- Statt ARP nutzt IPv6 **Neighbor Discovery** über ICMPv6.
- [[Routing (statisch, dynamisch, Inter-VLAN, Protokolle wie OSPF, RIP, BGP)]] arbeitet mit IPv6-Präfixen.
- [[IPv4 (Grundlagen & Subnetting usw..)]] bleibt wichtig, weil beide Protokolle lange parallel laufen.

## Eigene Worte (prüfungsnah)
IPv6 ist nicht einfach "IPv4 mit längerer Adresse", sondern ein moderneres Adresskonzept. Es gibt mehr Raum, klarere Präfixe, keine Broadcasts und oft eine automatische Adressbildung für Clients.

## Aufbau einer IPv6-Adresse
| Teil | Bedeutung |
|---|---|
| Präfix | Netzanteil |
| Interface Identifier | Hostanteil / Schnittstellenanteil |
| Länge | meist `/64` pro Subnetz |

Ein typisches Unternehmens- oder LAN-Subnetz nutzt **/64**. Das heißt:
- 64 Bit Netzanteil
- 64 Bit Interface-ID

## Wichtige Adresstypen
| Bereich | Bedeutung | Beispiel |
|---|---|---|
| `::1/128` | Loopback | lokale Selbstansprache |
| `fe80::/10` | Link-Local | nur im lokalen Segment |
| `fc00::/7` | Unique Local Address (ULA) | privat nutzbare Adressen |
| `2000::/3` | globale Unicast-Adressen | öffentlich routbar |
| `ff00::/8` | Multicast | Gruppenkommunikation |

## Wichtige Unterschiede zu IPv4
| Thema | IPv4 | IPv6 |
|---|---|---|
| Adresslänge | 32 Bit | 128 Bit |
| Schreibweise | dezimal in 4 Oktetten | hexadezimal in 8 Blöcken |
| Broadcast | vorhanden | nicht vorhanden |
| lokale Auflösung | ARP | Neighbor Discovery |
| typische Client-Adressvergabe | DHCP | SLAAC, DHCPv6 oder statisch |

## SLAAC, DHCPv6 und Link-Local
**SLAAC** bedeutet, dass ein Client aus Router-Informationen und eigener Kennung automatisch eine IPv6-Adresse bilden kann.

**Link-Local-Adressen** (`fe80::/10`) existieren praktisch immer und werden für lokale Kommunikation und Neighbor Discovery benötigt.

**DHCPv6** kann ergänzend genutzt werden, etwa für zentrale Verwaltung oder Zusatzinformationen.

## IPv6-Subnetting
Beim IPv6-Subnetting arbeitet man meist mit Präfixen wie `/48`, `/56` oder `/64`.

### Beispiel
Ein Unternehmen erhält das Präfix:
`2001:db8:1234::/48`

Wenn daraus `/64`-Netze gebildet werden:
- stehen `16` Bit für Subnetze zur Verfügung
- möglich sind `2^16 = 65.536` Subnetze

**Beispiel-Subnetze:**
- `2001:db8:1234:0001::/64`
- `2001:db8:1234:0002::/64`
- `2001:db8:1234:0003::/64`

## Beispielaufgabe mit Lösung
**Aufgabe:** Ein Unternehmen hat das Präfix `2001:db8:5000::/56`. Wie viele `/64`-Subnetze können daraus gebildet werden?

**Lösung:**
1. Von `/56` auf `/64` werden `8` zusätzliche Bits für Subnetze verwendet.
2. Anzahl der Subnetze: `2^8 = 256`

**Antwort:**
Aus einem `/56`-Präfix entstehen **256** Netze mit `/64`.

## Prüfungsthemen mit hoher Wahrscheinlichkeit
- IPv6-Schreibweise kürzen oder ausschreiben
- Link-Local, ULA und Global Unicast unterscheiden
- IPv4 und IPv6 vergleichen
- erklären, warum es in IPv6 keinen Broadcast gibt
- Präfixe in mögliche Teilnetze umrechnen

## Merksätze
- IPv6 hat 128 Bit und wird hexadezimal geschrieben.
- Ein normales LAN-Subnetz ist meist `/64`.
- IPv6 kennt Multicast statt Broadcast.
- Link-Local beginnt typischerweise mit `fe80`.
