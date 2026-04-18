# Domänenkonzepte

## Definition
**Domänenkonzepte** beschreiben, wie Verzeichnisdienste wie Active Directory logisch und geografisch aufgebaut werden. Wichtige Begriffe sind:
- **Domäne**
- **Tree**
- **Forest**
- **Site**
- **Replikation**

## Warum ist das so?
Kleine Unternehmen kommen oft mit einer einzelnen Domäne aus. Größere Organisationen haben aber:
- mehrere Standorte
- verschiedene Organisationseinheiten
- getrennte Verwaltungsbereiche
- hohe Anforderungen an Skalierung und Replikation

Darum braucht es strukturierte Konzepte für Aufbau und Vertrauensbeziehungen.

## Zusammenspiel
- [[Active Directory und LDAP]] liefert die Grundlage des Verzeichnisdiensts.
- [[Berechtigungskonzepte]] nutzt diese Strukturen für Rollen und Gruppen.
- [[Netzwerkrelevante Dienste (DHCP, DNS, NTP, SNMP...)]] ist wichtig für Namensauflösung und Zeitkonsistenz.
- [[Anforderungen an Bandbreite, Latenz, Verfügbarkeit, Übertragungsmedien und Netzwerksicherheit]] ist bei Replikation zwischen Standorten relevant.

## Eigene Worte (prüfungsnah)
Die Domäne ist die zentrale Verwaltungseinheit. Tree und Forest beschreiben größere logische Strukturen darüber. Sites beschreiben dagegen eher die physische oder standortbezogene Sicht, damit Replikation sinnvoll geplant werden kann.

## Wichtige Begriffe
| Begriff | Bedeutung |
|---|---|
| Domäne | grundlegender AD-Verwaltungsbereich |
| Tree | hierarchisch verbundene Domänen mit gemeinsamem Namensraum |
| Forest | oberste Gesamtstruktur, kann mehrere Trees enthalten |
| Site | physischer Standort bzw. replizierungstechnisch zusammengehöriger Bereich |
| Replikation | Abgleich von Verzeichnisänderungen zwischen DCs |

## Domäne, Tree und Forest
| Ebene | Beispiel |
|---|---|
| Domäne | `firma.local` |
| Tree | `firma.local`, `it.firma.local`, `sales.firma.local` |
| Forest | mehrere Trees unter gemeinsamer Gesamtstruktur |

## Sites und Replikation
Wenn Unternehmen mehrere Standorte haben, replizieren Domänencontroller Änderungen untereinander:
- neue Benutzer
- Passwortänderungen
- Gruppenmitgliedschaften

Die **Site-Konfiguration** hilft dabei, Replikation an WAN-Strecken und Standorte anzupassen.

## Typische Prüfungslogik
| Frage | passende Sicht |
|---|---|
| logische Verwaltungseinheit? | Domäne |
| mehrere Domänen in Hierarchie? | Tree |
| gesamte AD-Gesamtstruktur? | Forest |
| physischer Standort / Replikationsoptimierung? | Site |

## Beispielaufgabe mit Lösung
**Aufgabe:** Ein Unternehmen hat Standorte in Berlin und München. Beide nutzen dieselbe AD-Gesamtstruktur, aber Änderungen sollen standortgerecht repliziert werden. Welches Konzept ist hier besonders wichtig?

**Lösung:**
**Sites und Replikation**

**Begründung:**
Die Site-Struktur bildet physische Standorte ab und steuert, wie Verzeichnisdaten über WAN-Strecken repliziert werden.

## Typische Prüfungsszenarien
- Domäne, Tree und Forest unterscheiden.
- Site von Domäne abgrenzen.
- Replikation im AD erklären.
- Vertrauensbeziehungen grob einordnen.

## Merksätze
- Domäne = Verwaltungseinheit.
- Forest = oberste Gesamtstruktur.
- Site = physische Sicht für Replikation, nicht primär für Rechte.
