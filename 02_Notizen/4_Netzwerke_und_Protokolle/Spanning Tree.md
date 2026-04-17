# Spanning Tree

Das **Spanning Tree Protocol (STP)** arbeitet auf Layer 2 (Sicherungsschicht) des [[OSI und TCP-IP Modell|OSI-Modells]]. Es hat eine Hauptaufgabe: Es soll sogenannte **Switching-Loops** (Schleifen) im Netzwerk verhindern.

Schleifen entstehen, wenn Switches über redundante Pfade (mehrere Kabelwege) miteinander verbunden sind. Ein Broadcast-Paket würde ohne STP von Switch zu Switch im Kreis geschickt werden, sich vervielfachen und das Netzwerk durch einen "Broadcast-Storm" innerhalb von Sekunden komplett lahmlegen.

So arbeitet STP:
1. Die Switches tauschen Informationen über sogenannte **BPDUs** (Bridge Protocol Data Units) aus.
2. Es wird ein "Root-Bridge" als Chef-Switch des Netzes gewählt.
3. Der Algorithmus berechnet die besten, schleifenfreien Pfade durch das Netz.
4. Alle redundanten Backup-Pfade werden logisch blockiert.
5. Fällt der Hauptpfad aus, erkennt STP das und aktiviert den blockierten Backup-Pfad.

Moderne Netze nutzen Weiterentwicklungen wie **RSTP** (Rapid Spanning Tree), das bei Ausfällen wesentlich schneller umschaltet, oder **MSTP** (Multiple Spanning Tree), das getrennte Topologien pro VLAN erlaubt.

Querverbindungen: [[Netzwerktopologien und Netzwerkplane]], [[VLAN Arten, Trunking ....]] und [[OSI und TCP-IP Modell]].
