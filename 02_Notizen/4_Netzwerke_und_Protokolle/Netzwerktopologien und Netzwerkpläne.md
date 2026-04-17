# Netzwerktopologien und Netzwerkplane

**Netzwerktopologien** beschreiben die physische oder logische Anordnung von Geräten und Leitungen in einem Computernetzwerk.

Die wichtigsten Topologien für Prüfungen sind:
- **Stern-Topologie:** Alle Endgeräte sind mit einem zentralen Verteiler (heute ein Switch) verbunden. Fällt ein Kabel aus, betrifft das nur einen Client. Fällt der Switch aus, steht das ganze Netz. Dies ist heute der absolute Standard in lokalen Netzen.
- **Ring-Topologie:** Jedes Gerät ist mit genau zwei anderen verbunden. Nachrichten werden in eine Richtung durchgereicht. Heute selten, früher bei Token-Ring genutzt.
- **Bus-Topologie:** Alle Geräte hängen an einem Hauptstrang (dem Bus). Es kann zu Kollisionen kommen, da immer nur einer senden darf. Wird das Kabel durchtrennt, fällt das Netz aus.
- **Maschen-Topologie (Mesh):** Endgeräte oder Router sind mit mehreren oder allen anderen Geräten verbunden (vollvermascht). Das bietet extrem hohe Ausfallsicherheit, ist bei Kabeln aber sehr teuer. Im Internet und bei großen WLAN- oder Richtfunknetzen ist diese Topologie üblich.

**Netzwerkpläne** sind wichtig für die Dokumentation. Sie zeigen grafisch, welche Topologie herrscht, wo Router und Firewalls sitzen, wie [[VLAN Arten, Trunking ....|VLANs]] konfiguriert sind und welche IPs vergeben wurden. 
Verknüpfungen: [[LAN, WAN, WLAN ....]], [[Strukturierte Verkabelung Kupfer, Glasfaser, Funk, WLAN und Bluetooth]] und [[Spanning Tree]].
