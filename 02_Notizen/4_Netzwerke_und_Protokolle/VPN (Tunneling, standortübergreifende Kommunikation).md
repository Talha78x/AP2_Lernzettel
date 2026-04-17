# VPN Tunneling, standortubergreifende Kommunikation

Ein **VPN** (*Virtual Private Network*) verbindet räumlich getrennte Standorte oder einzelne Benutzer sicher über ein unsicheres Netz wie das Internet. Typische Einsatzfälle sind die Verbindung mehrerer Firmenstandorte oder der sichere Zugriff aus dem Homeoffice auf interne Ressourcen.

Beim **Tunneling** werden die ursprünglichen Daten in ein zusätzlich geschütztes Paket eingebettet. Von außen sind dabei im neuen äußeren Header meist nur noch die Adressen der VPN-Gateways sichtbar. Das verbessert die Abschirmung der internen Kommunikation.

Für standortübergreifende VPNs ist vor allem **IPSec** wichtig. IPSec arbeitet auf Layer 3 und verfolgt die klassischen Schutzziele:
- **Vertraulichkeit**
- **Integrität**
- **Authentizität**

Wichtige IPSec-Bausteine sind:
- **ESP** für Vertraulichkeit.
- **AH** für Integrität und Authentizität.
- Verfahren zur Authentifizierung, zum Beispiel über Schlüssel oder Zertifikate.

Im Unterschied dazu arbeitet [[TLS SSL]] höher im Protokollstapel. Darum ist es sinnvoll, [[VPN Tunneling, standortubergreifende Kommunikation]] immer zusammen mit [[TLS SSL]], [[NAT PAT]] und [[OSI und TCP-IP Modell]] zu lernen.

Merksatz: Ein VPN macht das Internet nicht privat, sondern baut über das öffentliche Internet einen **geschützten logischen Tunnel** für private Kommunikation auf.
