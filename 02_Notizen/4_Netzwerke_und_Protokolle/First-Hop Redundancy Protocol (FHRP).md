# First-Hop Redundancy Protocol (FHRP)

## Definition
**FHRP (First-Hop Redundancy Protocol)** ist eine Protokollfamilie zur Absicherung des **Default Gateways** in einem lokalen Netz oder VLAN. Ziel ist, dass Clients bei Ausfall eines Routers oder Layer-3-Gateways möglichst ohne manuelle Anpassung weiterarbeiten können.

## Warum ist das so?
Der Default Gateway ist für viele Clients der erste Schritt aus dem eigenen Netz. Fällt dieses Gateway aus, können Geräte oft nicht mehr in andere Netze kommunizieren, obwohl:
- der Client selbst funktioniert
- das lokale VLAN funktioniert
- der Server vielleicht sogar noch erreichbar wäre

FHRP beseitigt also einen klassischen Single Point of Failure am Netzrand.

## Zusammenspiel
- [[VLAN (Arten, Trunking ...)]]: häufig gibt es pro VLAN ein eigenes Default Gateway und damit auch FHRP-Gruppen.
- [[Routing (statisch, dynamisch, Inter-VLAN, Protokolle wie OSPF, RIP, BGP)]]: FHRP ergänzt Routing um Gateway-Redundanz.
- [[IPv4 (Grundlagen & Subnetting usw..)]] und [[IPv6 (Grundlagen & Subnetting usw..)]] liefern die Adressbasis.
- [[Snap-Shot, Versionierung, Hochverfügbarkeit (Clustering, Load Balancing, FHRP)]] ordnet FHRP in Hochverfügbarkeitskonzepte ein.

## Eigene Worte (prüfungsnah)
FHRP ist ein Ausfallsicherungs-Trick für das Standardgateway. Der Client kennt nur eine virtuelle Gateway-Adresse. Im Hintergrund stehen aber mehrere Router bereit. Fällt der aktive aus, übernimmt ein anderer.

## Grundprinzip
1. Mehrere Router bilden eine FHRP-Gruppe.
2. Die Gruppe besitzt eine **virtuelle IP-Adresse**.
3. Clients verwenden genau diese virtuelle IP als Default Gateway.
4. Einer ist aktiv, andere stehen bereit.
5. Bei Ausfall übernimmt ein anderer Router.

## Typische Protokolle
| Protokoll | Besonderheit |
|---|---|
| HSRP | Cisco-Protokoll, ein aktiver und ein Standby-Router |
| VRRP | standardisierter Ansatz, herstellerübergreifend |
| GLBP | verteilt zusätzlich Last auf mehrere Gateways |

## Wichtige Begriffe
| Begriff | Bedeutung |
|---|---|
| virtuelle IP | Gateway-Adresse, die der Client eingetragen bekommt |
| virtuelle MAC | MAC-Adresse der FHRP-Gruppe |
| aktiver Router | übernimmt aktuell die Gateway-Funktion |
| Standby / Backup | springt bei Ausfall ein |
| Preemption | Router mit höherer Priorität darf aktive Rolle zurückholen |

## Warum merken Clients den Wechsel oft nicht?
Weil für den Client dieselbe virtuelle Gateway-IP bestehen bleibt. Nur das Gerät im Hintergrund, das diese Rolle übernimmt, wechselt.

## Beispielaufgabe mit Lösung
**Aufgabe:** In VLAN 20 nutzen alle Clients das Gateway `192.168.20.254`. Tatsächlich stehen zwei Router bereit. Einer fällt aus, die Clients können trotzdem weiterarbeiten. Welches Konzept wird verwendet?

**Lösung:**
Ein **FHRP-Konzept**, zum Beispiel HSRP oder VRRP.

**Begründung:**
1. Die Clients nutzen eine gemeinsame virtuelle Gateway-Adresse.
2. Mehrere Router sichern diese Adresse redundant ab.
3. Beim Ausfall übernimmt ein anderer Router transparent.

## Typische Prüfungsszenarien
- erklären, warum FHRP für Hochverfügbarkeit wichtig ist.
- virtuelle IP und physische Router-IP unterscheiden.
- HSRP, VRRP und GLBP grob einordnen.
- FHRP von Routing-Protokollen abgrenzen.

## Merksätze
- FHRP schützt nicht das ganze Netz, sondern den ersten Router-Hop.
- Die virtuelle Gateway-IP bleibt gleich, der aktive Router kann wechseln.
- Routing und FHRP ergänzen sich, sind aber nicht dasselbe.
