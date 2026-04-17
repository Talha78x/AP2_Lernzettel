# URLs und DNS

**URL (Uniform Resource Locator):**
Eine URL ist die vollständige Adresse einer Ressource im Internet. Aufbau:
`schema://benutzer:passwort@host:port/pfad?abfrage#fragment`

Beispiel: `https://www.beispiel.de:443/produkte?id=5#details`
- `https` → Protokoll (Schema)
- `www.beispiel.de` → Hostname (FQDN)
- `443` → Port (wird bei HTTPS meist weggelassen, da Standard)
- `/produkte` → Pfad auf dem Webserver
- `?id=5` → Query-Parameter
- `#details` → Anker (Fragment, nur für den Browser)

**DNS-Auflösung (Resolver-Prozess):**
1. Browser prüft den lokalen Cache.
2. Browser fragt den konfigurierten DNS-Resolver (meist der Router oder ein Server wie `8.8.8.8`).
3. Der Resolver fragt hierarchisch die DNS-Infrastruktur: Root-Server → TLD-Server (`.de`) → Autoritativer Nameserver der Domain.
4. Die IP-Adresse wird zurückgeliefert und gecacht (TTL beachten).

Querverweise: [[Netzwerkrelevante Dienste (DHCP, DNS, NTP, SNMP...)]], [[Mail-Service (MX, A, AAAA..)]].
