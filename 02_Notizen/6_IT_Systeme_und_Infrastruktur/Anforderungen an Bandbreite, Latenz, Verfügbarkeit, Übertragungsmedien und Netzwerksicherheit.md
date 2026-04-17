# Anforderungen an Bandbreite, Latenz, Verfugbarkeit, Ubertragungsmedien und Netzwerksicherheit

Bei der Planung einer IT-Infrastruktur müssen FISIs verschiedene technische Anforderungen an das Netzwerk bewerten. Diese Faktoren entscheiden darüber, ob eine Anwendung flüssig läuft oder unbenutzbar wird.

- **Bandbreite:** Die maximal mögliche Datenübertragungsrate (z. B. 1 Gbit/s). Wichtig für große Dateitransfers (siehe [[Dateifreigaben und Datenabruf, z. B. SMB, CIFS und ODBC]]) oder Backups.
- **Latenz:** Die Verzögerungszeit, bis ein Datenpaket vom Sender beim Empfänger ankommt. Für Echtzeitanwendungen wie VoIP oder Datenbankabfragen ist eine niedrige Latenz oft wichtiger als eine hohe Bandbreite. Hier greifen oft [[QoS]]-Mechanismen.
- **Verfügbarkeit:** Wird in Prozent angegeben (z. B. 99,9 % entspricht ca. 8,7 Stunden Ausfallzeit pro Jahr). Sie wird durch redundante [[Server und Storage|Server]], Netzwerkkarten und Protokolle wie [[First-Hop Redundancy Protocol FHRP]] sichergestellt.
- **Übertragungsmedien:** Die Wahl zwischen Kupfer, Glasfaser oder Funk (siehe [[Strukturierte Verkabelung Kupfer, Glasfaser, Funk, WLAN und Bluetooth]]) hängt von der benötigten Distanz, Bandbreite und Störanfälligkeit ab.
- **Netzwerksicherheit:** Schutz vor unbefugtem Zugriff und Ausfällen. Umgesetzt durch [[Firewall IDS, IPS, DMZ, ACL, Filtertabelle]], [[VPN Tunneling, standortubergreifende Kommunikation]] und [[Zutritts-, Zugangs- und Zugriffskontrolle]].
