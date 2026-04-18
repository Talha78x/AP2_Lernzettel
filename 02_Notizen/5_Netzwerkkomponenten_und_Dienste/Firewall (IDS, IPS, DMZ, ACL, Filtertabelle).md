# Firewall (IDS, IPS, DMZ, ACL, Filtertabelle)

## Definition
Eine **Firewall** kontrolliert Netzwerkverkehr anhand definierter Regeln. Sie entscheidet, welcher Verkehr erlaubt, blockiert oder genauer geprüft wird. Firewalls schützen Netze, Systeme und Dienste vor ungewolltem Zugriff.

## Warum ist das so?
Nicht jeder Netzwerkverkehr ist erwünscht. Ohne Kontrolle könnten:
- interne Systeme direkt erreichbar sein
- unerlaubte Dienste offen stehen
- Angriffe ungehindert passieren
- Schadsoftware leichter kommunizieren

Eine Firewall schafft daher eine technische Kontrollinstanz an Netzgrenzen oder zwischen Sicherheitszonen.

## Zusammenspiel
- [[Netzwerkkomponenten]] ordnet Firewalls als zentrale Sicherheitskomponente ein.
- [[VLAN (Arten, Trunking ...)]] und Routing-Zonen werden oft über Firewall-Regeln miteinander verbunden oder getrennt.
- [[Schutzziele der IT]] liefert die Sicherheitsziele hinter Firewall-Konzepten.
- [[Firewall (IDS, IPS, DMZ, ACL, Filtertabelle)]] arbeitet häufig mit [[Routing (statisch, dynamisch, Inter-VLAN, Protokolle wie OSPF, RIP, BGP)]] und NAT zusammen.
- [[Zutritts-, Zugangs- und Zugriffskontrolle]] ergänzt die organisatorische Perspektive.

## Eigene Worte (prüfungsnah)
Eine Firewall ist der Türsteher des Netzwerks. Sie prüft nicht einfach nur "Internet ja oder nein", sondern bewertet Verkehrsregeln zwischen Quell- und Zieladresse, Ports, Protokollen und oft sogar Anwendungen.

## Firewall-Arten
| Art | Arbeitsweise | Vorteil | Nachteil |
|---|---|---|---|
| Paketfilter / Stateless | prüft jedes Paket einzeln | schnell, einfach | kein Verbindungsbezug |
| Stateful Firewall | merkt sich Verbindungszustände | praxistauglich, Standard | mehr Komplexität |
| Proxy / Application Gateway | terminiert und prüft Anwendungsprotokolle | tiefe Kontrolle | höherer Aufwand |
| NGFW | kombiniert mehrere Verfahren | sehr leistungsfähig | komplex und ressourcenintensiv |

## IDS und IPS
| Begriff | Bedeutung |
|---|---|
| IDS (Intrusion Detection System) | erkennt verdächtige Muster und meldet sie |
| IPS (Intrusion Prevention System) | erkennt und blockiert verdächtigen Verkehr aktiv |

**Merke:** IDS = melden, IPS = melden und eingreifen.

## ACL und Filtertabelle
Eine **ACL (Access Control List)** ist eine geordnete Regelliste. Typische Kriterien:
- Quell-IP
- Ziel-IP
- Protokoll
- Port
- Aktion erlauben oder verbieten

**Wichtig:** Regeln werden meist von oben nach unten geprüft. Das erste passende Match entscheidet.

## DMZ
Die **DMZ (Demilitarized Zone)** ist ein separates Netzsegment zwischen externem Netz und internem LAN.

Typische Systeme in der DMZ:
- Webserver
- Mail-Relay
- Reverse Proxy
- öffentliche Portale

**Warum DMZ?**
Falls ein öffentlich erreichbarer Server kompromittiert wird, ist das interne Netz besser abgeschirmt.

## Firewall im Zusammenspiel mit Zonen
| Zone | Typische Eigenschaft |
|---|---|
| Internet / untrusted | externe, unsichere Seite |
| DMZ | öffentlich erreichbare Dienste |
| internes LAN | besonders schützenswert |
| Management-Netz | stark eingeschränkt |

## Beispielaufgabe mit Lösung
**Aufgabe:** Ein Unternehmen möchte einen Webserver öffentlich erreichbar machen, ohne das interne Netz direkt freizugeben. Welche Netzstruktur ist passend?

**Lösung:**
Eine **DMZ** mit Firewall-Regeln.

**Begründung:**
1. Der Webserver wird in ein separates Segment gestellt.
2. Nur notwendige Zugriffe aus dem Internet werden erlaubt.
3. Das interne LAN bleibt zusätzlich geschützt und ist nicht direkt exponiert.

## Typische Prüfungsszenarien
- Firewall-Arten unterscheiden.
- IDS und IPS gegeneinander abgrenzen.
- DMZ erklären.
- ACL-Reihenfolge und Regelwirkung beschreiben.
- erklären, warum Firewall nicht gleich Antivirus ist.

## Merksätze
- Firewall regelt Verkehr, nicht nur "an oder aus".
- IDS erkennt, IPS blockiert.
- DMZ schützt das interne Netz vor öffentlich erreichbaren Diensten.
- Die Reihenfolge in ACLs ist entscheidend.
