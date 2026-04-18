# TLS & SSL

## Definition
**SSL (Secure Sockets Layer)** ist der historische Vorgänger von **TLS (Transport Layer Security)**. SSL gilt heute als veraltet und unsicher, während **TLS** der aktuelle Standard für abgesicherte Netzwerkverbindungen ist.

TLS schützt vor allem:
- **Vertraulichkeit** durch Verschlüsselung
- **Integrität** durch Manipulationsschutz
- **Authentizität** durch Zertifikate und Vertrauenskette

## Warum ist das so?
Ohne zusätzliche Absicherung könnten Anwendungsdaten im Netzwerk:
- mitgelesen
- verändert
- oder über gefälschte Gegenstellen abgefangen werden

TLS löst dieses Problem, indem vor der eigentlichen Datenübertragung ausgehandelt wird:
- wer die Gegenstelle ist
- welche kryptografischen Verfahren genutzt werden
- welche Sitzungsschlüssel verwendet werden

## Zusammenspiel
- [[Standardprotokolle (TCP, UDP, MAC, ARP, ICMP, HTTP, HTTPS, FTP, SMTP...)]] nutzt TLS zum Beispiel bei HTTPS.
- [[Zertifikate]] liefern die Grundlage für Vertrauensketten und Serverauthentifizierung.
- [[Hashverfahren & digitale Signaturen]] erklärt Hashing und Signaturprüfung im Hintergrund.
- [[Verschlüsselung (Arten, Symmetrisch, Asymmetrisch, Hybride)]] erklärt, warum TLS hybrid arbeitet.
- [[OSI und TCP-IP Modell]] hilft bei der Einordnung oberhalb der Transportebene.

## Eigene Worte (prüfungsnah)
TLS ist der Sicherheitsmantel einer Verbindung. HTTP allein überträgt Klartext. HTTPS bedeutet: HTTP läuft durch einen TLS-gesicherten Kanal. Der Client prüft zuerst, ob er dem Server vertrauen kann, und erst danach werden Daten verschlüsselt übertragen.

## SSL vs. TLS
| Punkt | SSL | TLS |
|---|---|---|
| Status | veraltet | aktueller Standard |
| Sicherheit | unsicher, nicht mehr einsetzen | modern und empfohlen |
| Einsatz heute | nur noch historisch relevant | Standard für Web und viele andere Dienste |

**Prüfungswichtig:** Wenn von "SSL-Zertifikat" gesprochen wird, ist in der Praxis fast immer ein Zertifikat für TLS gemeint.

## Ablauf einer TLS-gesicherten Verbindung
### Vereinfacht
1. Client baut über TCP eine Verbindung zum Server auf.
2. Client und Server handeln TLS-Version und Cipher Suites aus.
3. Der Server sendet sein Zertifikat.
4. Der Client prüft:
   - ist das Zertifikat gültig?
   - passt der Name?
   - ist die Zertifikatskette vertrauenswürdig?
5. Beide Seiten leiten gemeinsame Sitzungsschlüssel ab.
6. Danach werden Anwendungsdaten symmetrisch verschlüsselt übertragen.

## Warum hybrid?
TLS nutzt mehrere Verfahren zusammen:
- **asymmetrische Kryptografie** für Authentifizierung und Schlüsselaustausch
- **symmetrische Verschlüsselung** für schnelle Datenübertragung
- **Hash-/MAC-Verfahren** für Integrität

Genau dieses Zusammenspiel macht TLS effizient und sicher.

## TLS 1.2 vs. TLS 1.3
| Punkt | TLS 1.2 | TLS 1.3 |
|---|---|---|
| Aushandlung | komplexer | vereinfacht |
| Geschwindigkeit | mehr Round-Trips | schnellerer Handshake |
| ältere Verfahren | teils noch möglich | viele unsichere Altverfahren entfernt |
| Sicherheit | gut bei sauberer Konfiguration | moderner und sicherer |

**Merksatz:** TLS 1.3 ist schlanker, schneller und härter gegen Fehlkonfigurationen.

## Zertifikatsprüfung im Zusammenspiel
Der Client vergleicht:
- Domainname im Zertifikat mit der aufgerufenen Adresse
- Gültigkeitszeitraum
- Signaturkette bis zu einer vertrauenswürdigen CA

Wenn diese Prüfung fehlschlägt, meldet der Browser eine Warnung oder blockiert die Verbindung.

## Abgrenzung zu anderen Sicherheitsverfahren
| Verfahren | Schutzebene | Typischer Einsatz |
|---|---|---|
| TLS | Anwendungsnahe Verbindung | HTTPS, IMAPS, SMTPS |
| IPsec / [[VPN (Tunneling, standortübergreifende Kommunikation)]] | Netzwerkschicht | Standortvernetzung |
| SSH | sicherer Fernzugriff auf Anwendungsebene | Remote-Login, SCP, SFTP |

## Beispielaufgabe mit Lösung
**Aufgabe:** Warum reicht es für HTTPS nicht aus, einfach nur Port `443` zu verwenden?

**Lösung:**
Port `443` allein bewirkt keine Sicherheit. Erst wenn auf dieser TCP-Verbindung tatsächlich **TLS** verwendet wird, werden:
1. der Server authentifiziert,
2. Sitzungsschlüssel ausgehandelt,
3. Daten verschlüsselt und gegen Manipulation geschützt.

**Prüfungsnahe Kurzantwort:**
HTTPS ist nicht "HTTP auf Port 443", sondern **HTTP über TLS**.

## Typische Prüfungsszenarien
- TLS und SSL unterscheiden.
- erklären, warum Zertifikate nötig sind.
- TLS 1.2 und 1.3 grob vergleichen.
- HTTPS, VPN und SSH voneinander abgrenzen.
- beschreiben, wie ein Client das Serverzertifikat prüft.

## Merksätze
- SSL ist alt, TLS ist aktuell.
- TLS schützt Vertraulichkeit, Integrität und Authentizität.
- HTTPS = HTTP plus TLS.
- Ein Zertifikat ist nur dann nützlich, wenn die Vertrauenskette auch geprüft wird.
