# Netzwerkrelevante Dienste (DHCP, DNS, NTP, SNMP...)

Netzwerkdienste laufen meist unsichtbar im Hintergrund, sind aber absolut essenziell. Fallen sie aus, funktioniert das gesamte Netzwerk nicht mehr.

**DHCP (Dynamic Host Configuration Protocol) – Port 67/68 UDP:**
Verteilt automatisch IP-Adressen, Subnetzmasken, Standard-Gateway und DNS-Server-Adressen an Clients. Ablauf: DORA (Discover → Offer → Request → Acknowledge). Ohne DHCP müsste jeder Rechner manuell konfiguriert werden.

**DNS (Domain Name System) – Port 53 UDP/TCP:**
Übersetzt Domainnamen (z.B. `www.google.de`) in IP-Adressen (A-Record für IPv4, AAAA-Record für IPv6). Ohne DNS müsste man jede IP-Adresse auswendig kennen. Weitere wichtige Record-Typen: MX (Mail), CNAME (Alias), PTR (Reverse Lookup).

**NTP (Network Time Protocol) – Port 123 UDP:**
Synchronisiert die Systemuhren aller Geräte im Netz auf eine gemeinsame Zeit. Absolut kritisch für: Kerberos-Authentifizierung (max. 5 Minuten Zeitabweichung erlaubt!), Log-Korrelation (siehe [[Event-Logs, Syslog]]) und digitale Zertifikate (Gültigkeit).

**SNMP (Simple Network Management Protocol) – Port 161/162 UDP:**
Dient der Netzwerküberwachung. Wird separat behandelt in [[Monitoring und SNMP]].

Querverweise: [[URLs und DNS]], [[Monitoring und SNMP]], [[Active Directory und LDAP]].
