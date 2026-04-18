# Virtualisierung (Bare-Metal, Hypervisor, Container)

## Definition
**Virtualisierung** trennt logische Systeme von der physischen Hardware. Dadurch können mehrere virtuelle Umgebungen auf derselben Hardware betrieben werden.

Wichtige Konzepte:
- **Hypervisor**
- **virtuelle Maschinen (VMs)**
- **Container**

## Warum ist das so?
Physische Server würden ohne Virtualisierung oft schlecht ausgelastet sein. Virtualisierung ermöglicht:
- bessere Ressourcennutzung
- schnellere Bereitstellung
- einfachere Trennung von Diensten
- flexible Test- und Produktivumgebungen

## Zusammenspiel
- [[Server und Storage]] liefert die physische Basis.
- [[On-Premises, Cloud, Housing, Hosting sowie IaaS, PaaS und SaaS]] baut technisch oft auf Virtualisierung auf.
- [[Deploymentstrategien]] profitieren von standardisierten Images und Containern.
- [[2-Tier-, 3-Tier- und Multi-Tier-Architekturen]] können als getrennte VMs oder Container bereitgestellt werden.

## Eigene Worte (prüfungsnah)
Virtualisierung macht aus einer physischen Maschine mehrere logisch getrennte Systeme. Bei klassischen VMs bringt jedes System ein eigenes Gastbetriebssystem mit, bei Containern teilen sich mehrere Instanzen denselben Host-Kernel.

## Hypervisor-Typen
| Typ | Beschreibung | Beispielhafter Einsatz |
|---|---|---|
| Typ 1 / Bare-Metal | läuft direkt auf der Hardware | Rechenzentrum, produktive Server |
| Typ 2 / Hosted | läuft auf einem Host-Betriebssystem | Test, Entwicklung, Desktop |

## Virtuelle Maschinen
| Merkmal | VM |
|---|---|
| eigenes Gastbetriebssystem | ja |
| Isolation | hoch |
| Startzeit | eher höher |
| Ressourcenbedarf | höher als Container |

## Container
| Merkmal | Container |
|---|---|
| eigener Kernel | nein, Host-Kernel wird geteilt |
| Startzeit | sehr schnell |
| Ressourcenbedarf | gering |
| Isolation | leichter als bei VMs |

## VM vs. Container
| Frage | VM | Container |
|---|---|---|
| braucht eigenes Gast-OS? | ja | nein |
| stärker isoliert? | ja | meist nein, aber ausreichend für viele Einsätze |
| leichtergewichtig? | nein | ja |
| typisch für | klassische Serverkonsolidierung | moderne App-Bereitstellung, Microservices |

## Beispielaufgabe mit Lösung
**Aufgabe:** Eine Anwendung soll sehr schnell startbar sein und nur ihre direkten Abhängigkeiten mitbringen, ohne jedes Mal ein komplettes Gastbetriebssystem zu starten. Welche Technik passt?

**Lösung:**
**Container**

**Begründung:**
1. Container teilen sich den Host-Kernel.
2. Sie sind leichtgewichtig.
3. Sie starten deutlich schneller als klassische VMs.

## Typische Prüfungsszenarien
- Hypervisor Typ 1 und Typ 2 unterscheiden.
- VM und Container abgrenzen.
- erklären, warum Container ressourcenschonender sind.
- Virtualisierung als Basis von Cloud und Serverkonsolidierung beschreiben.

## Merksätze
- Bare-Metal-Hypervisor läuft direkt auf der Hardware.
- VMs bringen ein eigenes OS mit, Container meist nicht.
- Container sind schneller und leichter, VMs meist stärker isoliert.
