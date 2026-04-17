# Virtualisierung Bare-Metal, Hypervisor, Container

Virtualisierung entkoppelt Software von Hardware, um Ressourcen (CPU, RAM) effizienter zu nutzen. Kernkomponente ist der **Hypervisor** (Virtual Machine Monitor), der die Ressourcen der physischen Maschine auf virtuelle Maschinen (VMs) verteilt.

**Hypervisor-Typen:**
- **Typ 1 (Bare-Metal):** Der Hypervisor (z. B. VMware ESXi, Microsoft Hyper-V, Proxmox) wird *direkt* auf die leere Server-Hardware installiert. Er benötigt kein darunterliegendes volles Betriebssystem. Bietet höchste Performance und Stabilität, ist aber hardwareabhängig. Der Standard in Rechenzentren.
- **Typ 2 (Hosted):** Der Hypervisor (z. B. VMware Workstation, Oracle VirtualBox) wird als normales Programm auf einem bereits installierten Host-Betriebssystem (z. B. Windows 11) ausgeführt. Weniger performant durch den Overhead des Host-OS, aber flexibel für Entwickler oder Tests am Desktop-PC.

**Container-Virtualisierung (z. B. Docker):**
Im Gegensatz zu klassischen VMs, bei denen jede VM ein eigenes, komplettes Gast-Betriebssystem mitbringt, teilen sich Container den Kernel des Host-Betriebssystems.
- *Vorteile:* Container sind extrem leichtgewichtig, starten in Sekunden, verbrauchen wenig RAM und enthalten nur die Anwendung inklusive ihrer direkten Abhängigkeiten (Libraries).
- *Nachteile:* Sie sind weniger stark voneinander isoliert als klassische VMs. 

Querverweise: [[On-Premises, Cloud, Housing, Hosting sowie IaaS, PaaS und SaaS]], [[Deploymentstrategien]].
