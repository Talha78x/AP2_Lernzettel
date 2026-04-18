# Server und Storage

## Definition
**Server** stellen Dienste, Anwendungen oder Ressourcen für andere Systeme bereit. **Storage** bezeichnet Speicherlösungen, mit denen Daten lokal oder über das Netzwerk bereitgestellt werden.

## Warum ist das so?
In Unternehmensumgebungen reichen einzelne Arbeitsplatzrechner für zentrale Dienste nicht aus. Es braucht Systeme, die:
- dauerhaft verfügbar sind
- mehrere Benutzer bedienen
- große Datenmengen speichern
- zuverlässig und redundant arbeiten

Darum unterscheidet man Serverrollen und Speicherarchitekturen.

## Zusammenspiel
- [[Client-Server und Peer-to-Peer]] liefert das Grundmodell für Serverdienste.
- [[Virtualisierung (Bare-Metal, Hypervisor, Container)]] nutzt Server- und Storage-Ressourcen effizient.
- [[RAID (Arten, Vor- und Nachteile)]] ergänzt Storage um Redundanz auf Datenträgerebene.
- [[Band, Platte, NAS, SAN, Cloud, USB und optische Datenträger als Sicherungsmedien]] grenzt Produktivspeicher von Backup-Medien ab.
- [[2-Tier-, 3-Tier- und Multi-Tier-Architekturen]] setzt Serverrollen architektonisch ein.

## Eigene Worte (prüfungsnah)
Ein Server ist ein spezialisierter Dienstbereitsteller. Storage ist die strukturierte Speicherbasis dafür. Nicht jeder Speicher ist gleich: Manche Lösungen liefern Dateien, andere Blockspeicher für Server oder Virtualisierung.

## Typische Servermerkmale
| Merkmal | Bedeutung |
|---|---|
| Redundanz | z. B. doppelte Netzteile oder mehrere NICs |
| ECC-RAM | erkennt und korrigiert Speicherfehler |
| Dauerbetrieb | für 24/7-Betrieb ausgelegt |
| Fernverwaltung | Verwaltung ohne physischen Zugriff |

## Speicherarten
| Art | Bedeutung | Typischer Einsatz |
|---|---|---|
| DAS | Direct Attached Storage, direkt am Server | kleiner oder lokaler Speicher |
| NAS | Network Attached Storage, Dateiebene | Dateifreigaben, Teamdaten |
| SAN | Storage Area Network, Blockebene | Virtualisierung, Datenbanken |

## NAS und SAN unterscheiden
| Merkmal | NAS | SAN |
|---|---|---|
| Zugriffsebene | Datei | Block |
| Protokolle | SMB, NFS | iSCSI, Fibre Channel |
| Nutzung | Dateiablage | Server-/VM-Speicher |
| Komplexität | eher einfacher | eher komplexer |

## Typische Einsätze
| Bedarf | passende Lösung |
|---|---|
| gemeinsame Ordner im Büro | NAS |
| Storage für viele virtuelle Maschinen | SAN |
| lokaler Speicher im Einzelserver | DAS |

## Beispielaufgabe mit Lösung
**Aufgabe:** Eine Virtualisierungsumgebung benötigt zentralen, performanten Speicher auf Blockebene für mehrere Hosts. Welche Lösung passt am besten?

**Lösung:**
Ein **SAN**.

**Begründung:**
1. Es stellt Speicher auf Blockebene bereit.
2. Mehrere Hosts können darauf zugreifen.
3. Solche Szenarien sind typisch für Virtualisierung und performante Serverumgebungen.

## Typische Prüfungsszenarien
- Server von Arbeitsplatzsystemen abgrenzen.
- NAS und SAN unterscheiden.
- Datei- und Blockebene erklären.
- Redundanzmerkmale von Serverhardware nennen.

## Merksätze
- NAS liefert Dateien, SAN liefert Blöcke.
- Serverhardware ist auf Verfügbarkeit und Dauerbetrieb ausgelegt.
- Speicher für Produktivbetrieb ist nicht automatisch Backup.
