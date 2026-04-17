# Mail-Service (MX, A, AAAA..)

E-Mail ist nach wie vor das kritischste Kommunikationsmedium im Unternehmensalltag. FISIs müssen die DNS-Einträge kennen, die für den Mail-Fluss verantwortlich sind.

**DNS-Record-Typen im Kontext Mail:**
- **MX-Record (Mail Exchanger):** Gibt an, welcher Mailserver für eine Domain zuständig ist (z.B. `firma.local → mail.firma.local`). Er hat eine Priorität (niedrigerer Wert = bevorzugt).
- **A-Record:** Löst einen Hostnamen in eine IPv4-Adresse auf (z.B. `mail.firma.local → 192.168.1.10`). Wird benötigt, damit der MX-Eintrag auch tatsächlich erreichbar ist.
- **AAAA-Record:** Wie der A-Record, aber für IPv6-Adressen.
- **PTR-Record (Reverse DNS):** Die Umkehrung des A-Records: Löst eine IP-Adresse in einen Hostnamen auf. Für Mailserver extrem wichtig, da viele empfangende Mailserver eingehende E-Mails ablehnen (als Spam markieren), wenn für die sendende IP kein gültiger PTR-Eintrag existiert.
- **SPF-Record (TXT):** Legt fest, welche Server berechtigt sind, E-Mails im Namen der Domain zu senden. Schutz vor E-Mail-Spoofing.

Querverweise: [[URLs und DNS]], [[Netzwerkrelevante Dienste (DHCP, DNS, NTP, SNMP...)]].
