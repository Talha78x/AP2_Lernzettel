# IPv4 (Grundlagen & Subnetting usw..)

## Definition
**IPv4** ist das klassische Internet-Protokoll der Schicht 3. Eine IPv4-Adresse ist **32 Bit** lang und wird meist in **vier Oktetten** dargestellt, zum Beispiel `192.168.10.25`.

Eine IPv4-Adresse besteht immer aus:
- **Netzanteil**
- **Hostanteil**

Welche Bits zum Netz und welche zum Host gehören, legt die **Subnetzmaske** oder das **CIDR-Präfix** fest, zum Beispiel `/24`.

## Warum ist das so?
In Netzwerken müssen Geräte eindeutig adressiert werden. Gleichzeitig sollen Geräte sinnvoll gruppiert werden, damit Router wissen:
- was lokal ist
- was in ein anderes Netz weitergeleitet werden muss
- wie Broadcast-Domänen begrenzt werden

Subnetting ist also keine "Matheübung", sondern die technische Grundlage für Struktur, Sicherheit und Routing.

## Zusammenspiel
- [[OSI und TCP-IP Modell]] ordnet IPv4 auf Schicht 3 ein.
- [[Standardprotokolle (TCP, UDP, MAC, ARP, ICMP, HTTP, HTTPS, FTP, SMTP...)]] nutzt IPv4 als logische Adressbasis.
- [[NAT & PAT]] arbeitet mit IPv4-Adressen und Ports.
- [[Routing (statisch, dynamisch, Inter-VLAN, Protokolle wie OSPF, RIP, BGP)]] entscheidet anhand des Netzanteils über den Weg.
- [[IPv6 (Grundlagen & Subnetting usw..)]] ist der Nachfolger mit 128 Bit.

## Eigene Worte (prüfungsnah)
IPv4 ist die Hausnummer eines Geräts im Netzwerk. Das Präfix sagt dabei, welcher Teil zur Straße gehört und welche Nummer das einzelne Haus hat. Subnetting bedeutet: Ich teile eine große Straße in kleinere, besser verwaltbare Abschnitte auf.

## Aufbau einer IPv4-Adresse
| Teil | Bedeutung | Beispiel bei `192.168.10.25/24` |
|---|---|---|
| 32 Bit gesamt | gesamte Adresse | `192.168.10.25` |
| Netzanteil | identifiziert das Subnetz | `192.168.10` |
| Hostanteil | identifiziert das Gerät | `25` |
| Präfix `/24` | 24 Bit Netz, 8 Bit Host | Maske `255.255.255.0` |

## Wichtige Sonderbereiche
| Bereich | Bedeutung |
|---|---|
| `127.0.0.0/8` | Loopback |
| `169.254.0.0/16` | Link-Local / APIPA |
| `10.0.0.0/8` | privater Bereich |
| `172.16.0.0/12` | privater Bereich |
| `192.168.0.0/16` | privater Bereich |
| `224.0.0.0/4` | Multicast |
| `255.255.255.255` | lokaler Broadcast |

## APIPA / Link-Local
Wenn ein Client keine Adresse von [[Netzwerkrelevante Dienste (DHCP, DNS, NTP, SNMP...)|DHCP]] erhält, vergibt er sich oft selbst eine Adresse aus `169.254.0.0/16`.

**Bedeutung in der Praxis:**
- zeigt häufig ein DHCP-Problem an
- Kommunikation ist meist nur lokal im selben Segment möglich
- kein regulärer Ersatz für sauber geplante Adressierung

## Früher: Klassen A, B, C
Die Klassenadressierung ist historisch wichtig und wird in Prüfungen noch gern abgefragt.

| Klasse | Erster Oktettbereich | Standardmaske | Typische Größe |
|---|---|---|---|
| A | `1-126` | `255.0.0.0` | sehr große Netze |
| B | `128-191` | `255.255.0.0` | mittlere Netze |
| C | `192-223` | `255.255.255.0` | kleine Netze |

**Heute wichtiger:** CIDR und Subnetting statt starre Klassenlogik.

## Subnetting-Grundlagen
| Präfix | Maske | Host-Bits | Nutzbare Hosts |
|---|---|---|---|
| /24 | 255.255.255.0 | 8 | 254 |
| /25 | 255.255.255.128 | 7 | 126 |
| /26 | 255.255.255.192 | 6 | 62 |
| /27 | 255.255.255.224 | 5 | 30 |
| /28 | 255.255.255.240 | 4 | 14 |
| /29 | 255.255.255.248 | 3 | 6 |
| /30 | 255.255.255.252 | 2 | 2 |

**Formel:**
`nutzbare Hosts = 2^(Host-Bits) - 2`

Die `-2` stehen für:
- **Netzwerkadresse**: alle Host-Bits = `0`
- **Broadcastadresse**: alle Host-Bits = `1`

## Rechenweg beim Subnetting
### Beispielnetz `192.168.10.0/26`
| Punkt | Ergebnis |
|---|---|
| Präfix | `/26` |
| Maske | `255.255.255.192` |
| Host-Bits | `6` |
| Nutzbare Hosts | `2^6 - 2 = 62` |
| Blockgröße | `256 - 192 = 64` |
| Netzadresse | `192.168.10.0` |
| erster Host | `192.168.10.1` |
| letzter Host | `192.168.10.62` |
| Broadcast | `192.168.10.63` |

**Weitere /26-Netze im gleichen /24:**
- `192.168.10.0/26`
- `192.168.10.64/26`
- `192.168.10.128/26`
- `192.168.10.192/26`

## Beispielaufgabe mit Lösung
**Aufgabe:** Ein Netz `192.168.50.0/24` soll in vier gleich große Subnetze aufgeteilt werden. Wie lauten Präfix, Maske und die ersten vier Netzadressen?

**Lösung:**
1. Vier Subnetze bedeuten `2` zusätzliche Netz-Bits.
2. Aus `/24` wird `/26`.
3. Neue Maske: `255.255.255.192`.
4. Blockgröße im letzten Oktett: `64`.

**Subnetze:**
- `192.168.50.0/26`
- `192.168.50.64/26`
- `192.168.50.128/26`
- `192.168.50.192/26`

**Je Subnetz nutzbare Hosts:**
`2^6 - 2 = 62`

## Typische Prüfungsszenarien
- Netzwerk-, Host- und Broadcastadresse berechnen.
- APIPA erklären.
- private, öffentliche und Multicast-Bereiche unterscheiden.
- Klassenwissen von modernem CIDR unterscheiden.
- passende Präfixlänge für eine Hostanzahl bestimmen.

## Merksätze
- IPv4 hat 32 Bit und vier Oktette.
- Subnetting leiht Bits vom Hostanteil an den Netzanteil aus.
- APIPA deutet oft auf fehlendes DHCP hin.
- Routing arbeitet mit dem Netzanteil, nicht mit dem Hostnamen.
