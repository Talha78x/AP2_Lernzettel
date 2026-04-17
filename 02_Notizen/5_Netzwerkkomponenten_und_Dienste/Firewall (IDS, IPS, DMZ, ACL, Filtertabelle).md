# Firewall (IDS, IPS, DMZ, ACL, Filtertabelle)

Eine Firewall ist das zentrale Sicherheitssystem an den Netzwerkgrenzen. Sie kontrolliert den ein- und ausgehenden Datenverkehr anhand von Regeln.

**Firewall-Arten:**
- **Paketfilter-Firewall (Stateless):** Prüft jedes Paket einzeln anhand von Quell-/Ziel-IP, Port und Protokoll. Schnell, aber ohne Kontext (weiß nicht, ob ein Paket zu einer erlaubten Verbindung gehört).
- **Stateful Inspection Firewall:** Merkt sich den Zustand von Verbindungen (Connection Table). Erlaubt automatisch Antwortpakete einer genehmigten Anfrage. Standard in modernen Umgebungen.
- **Proxy-Firewall (Application Gateway):** Versteht Protokolle auf Layer 7 (HTTP, FTP). Baut die Verbindung selbst auf und prüft den Inhalt.
- **NGFW (Next-Generation Firewall):** Kombination aus allem: Stateful Inspection + IDS/IPS + Deep Packet Inspection + Anwendungskontrolle.

**IDS / IPS:**
- *IDS (Intrusion Detection System):* Überwacht den Netzwerkverkehr passiv und **meldet** verdächtige Muster (Alarm), greift aber nicht ein.
- *IPS (Intrusion Prevention System):* Wie das IDS, aber es **blockiert** den Angriffs-Traffic aktiv in Echtzeit.

**DMZ (Demilitarisierte Zone):**
Ein separates Netzwerksegment zwischen dem Internet und dem internen LAN (oft mit zwei Firewalls realisiert). Öffentlich erreichbare Server (Webserver, Mail-Relay) werden in der DMZ platziert. So ist das interne Netz auch dann geschützt, wenn ein DMZ-Server kompromittiert wird.

**ACL (Access Control List):**
Eine geordnete Liste von Erlaubt/Verweigert-Regeln, die direkt auf Router- oder Switch-Interfaces angewendet wird. Jede Regel prüft Pakete von oben nach unten – das erste Match gewinnt.

Querverweise: [[Netzwerkkomponenten]], [[VLAN Arten, Trunking ...]], [[Schutzziele der IT]].
