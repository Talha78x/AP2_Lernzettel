# Snap-Shot, Versionierung, Hochverfugbarkeit Clustering, Load Balancing, FHRP

Um geschäftskritische Anwendungen vor Ausfällen zu schützen, werden verschiedene Konzepte zur Hochverfügbarkeit (High Availability, HA) eingesetzt. 

**Snapshots & Versionierung:**
- Ein **Snapshot** "friert" den Zustand eines Dateisystems oder einer [[Virtualisierung Bare-Metal, Hypervisor, Container|virtuellen Maschine]] zu einem exakten Zeitpunkt ein. Dies geschieht oft durch *Copy-on-Write* (es wird nur gespeichert, was sich ab diesem Moment ändert). Ein Snapshot ist *kein* vollwertiges Backup, sondern dient dem schnellen Zurückrollen (z. B. vor einem Software-Update).
- **Versionierung:** Speichert gezielt alte Stände von Dokumenten ab, sodass Benutzer (z. B. auf einem Dateiserver) versehentlich gelöschte oder überschriebene Dateien selbst wiederherstellen können.

**Hochverfügbarkeit & Clustering:**
- Ein **Cluster** ist ein Verbund mehrerer Server (Knoten/Nodes), die nach außen wie ein einziges System wirken.
- *Active/Active-Cluster:* Alle Server arbeiten gleichzeitig. Fällt einer aus, übernehmen die restlichen die Last. 
- *Active/Passive-Cluster (Failover):* Ein Server arbeitet, der andere ist im Standby und springt nur bei einem Ausfall ein (vergleiche [[First-Hop Redundancy Protocol FHRP]] auf Netzwerkebene).

**Load Balancing (Lastenverteilung):**
Ein Load Balancer steht als "Türsteher" vor einem Server-Cluster. Er nimmt z. B. Web-Anfragen entgegen und verteilt sie nach bestimmten Algorithmen (z. B. *Round Robin* = immer abwechselnd, oder *Least Connections* = an den Server mit der geringsten Last) auf die dahinterliegenden Webserver. Das erhöht die Performance und bietet Ausfallsicherheit.

Querverweise: [[Virtualisierung Bare-Metal, Hypervisor, Container]], [[Notfallkonzept, Disaster Recovery]].
