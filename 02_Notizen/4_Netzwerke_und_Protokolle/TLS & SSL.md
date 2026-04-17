# TLS SSL

**SSL** ist der ältere Vorgänger, **TLS** der heute übliche Standard für verschlüsselte Verbindungen auf höherer Protokollebene. Im Alltag begegnet TLS vor allem bei **HTTPS** über Port 443.

TLS sorgt dafür, dass Daten zwischen Kommunikationspartnern vertraulich übertragen werden und dass die Gegenstelle über **Zertifikate** überprüfbar ist. Dadurch schützt TLS unter anderem vor dem Mitlesen unverschlüsselter Verbindungen und erschwert **Man-in-the-Middle-Angriffe**.

Wichtige Merkpunkte:
- TLS schützt vor allem **Anwendungsdaten**.
- HTTPS ist HTTP **mit** TLS.
- Zertifikate und eine **PKI** helfen bei der Authentifizierung.
- Ohne gültige Vertrauenskette ist eine Verbindung verdächtig.

Für die Prüfung sollte man TLS gut von [[VPN Tunneling, standortubergreifende Kommunikation]] beziehungsweise IPSec abgrenzen:
- **IPSec** schützt auf Layer 3 den IP-Verkehr.
- **TLS** schützt auf höherer Ebene einzelne Verbindungen oder Anwendungen.

Das Thema hängt eng mit [[Standardprotokolle TCP, UDP, MAC, ARP, ICMP, HTTP, HTTPS, FTP, SMTP....]], [[OSI und TCP-IP Modell]] und [[Zertifikate]] zusammen.
