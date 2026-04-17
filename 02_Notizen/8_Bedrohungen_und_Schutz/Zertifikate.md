# Zertifikate

Zertifikate sind digitale Ausweise, die die Identität einer Person, eines Servers oder eines Unternehmens in der digitalen Welt bestätigen. Sie bilden das Fundament für sichere Verbindungen wie [[TLS SSL]] (HTTPS) oder [[VPN Tunneling, standortubergreifende Kommunikation|IPSec]].

**Inhalt eines Zertifikats (oft im X.509-Standard):**
- Angaben zum Inhaber (z.B. Domainname des Webservers).
- Der **Public Key** des Inhabers.
- Gültigkeitsdauer.
- Die [[Hashverfahren digitale Signaturen|digitale Signatur]] der ausstellenden Zertifizierungsstelle (CA).

**PKI (Public Key Infrastructure):**
Eine PKI ist das hierarchische System aus Hardware, Software und Prozessen, das Zertifikate ausstellt, verwaltet und widerruft.
- **Root CA (Wurzelzertifizierungsstelle):** Die oberste, absolut vertrauenswürdige Instanz. Ihr Zertifikat ist im Browser oder Betriebssystem fest vorinstalliert.
- **Sub CA (Zwischenzertifizierungsstelle):** Stellt im Auftrag der Root CA die eigentlichen Zertifikate für Endkunden aus (erhöht die Sicherheit, da die Root CA offline genommen werden kann).
- **CRL (Certificate Revocation List):** Eine Sperrliste für Zertifikate, die vor Ablauf ihrer Gültigkeit ungültig wurden (z.B. weil der Private Key gestohlen wurde).

Für Prüfungen ist die Vertrauenskette (Chain of Trust) wichtig: Man vertraut einem Server-Zertifikat nur, weil man der CA vertraut, die es digital signiert hat.

Querverweise: [[Verschlusselung Arten, Symmetrisch, Asymmetrisch, Hybride]], [[Hashverfahren digitale Signaturen]].
