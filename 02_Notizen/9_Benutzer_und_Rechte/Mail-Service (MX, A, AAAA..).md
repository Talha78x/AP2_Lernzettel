# Mail-Service (MX, A, AAAA..)

## Definition
Mail-Dienste im Internet funktionieren nur, wenn mehrere DNS-Einträge korrekt zusammenspielen. Besonders wichtig sind:
- **MX**
- **A**
- **AAAA**
- **PTR**
- **SPF** (oft als TXT-Eintrag)

## Warum ist das so?
E-Mails werden nicht einfach "an eine Domain" geschickt, sondern an konkrete Mailserver. Damit das funktioniert, müssen sendende Systeme wissen:
- welcher Mailserver zuständig ist
- unter welcher IP dieser erreichbar ist
- ob die sendende Seite vertrauenswürdig wirkt

Darum sind Maildienste stark von DNS abhängig.

## Zusammenspiel
- [[URLs und DNS]] erklärt die allgemeine Namensauflösung.
- [[Netzwerkrelevante Dienste (DHCP, DNS, NTP, SNMP...)]] ordnet DNS als Basisdienst ein.
- [[Standardprotokolle (TCP, UDP, MAC, ARP, ICMP, HTTP, HTTPS, FTP, SMTP...)]] ergänzt die Protokollseite, vor allem SMTP.
- [[Zertifikate]] und [[TLS & SSL]] sind bei verschlüsselter Mailkommunikation relevant.

## Eigene Worte (prüfungsnah)
Mail im DNS heißt: Der MX-Eintrag sagt, welcher Server zuständig ist. A- oder AAAA-Einträge sagen, wie man ihn technisch erreicht. PTR und SPF helfen zusätzlich dabei, Vertrauen und Seriosität beim Versand zu verbessern.

## Wichtige Record-Typen
| Record | Aufgabe |
|---|---|
| MX | zuständiger Mailserver für eine Domain |
| A | Hostname zu IPv4-Adresse |
| AAAA | Hostname zu IPv6-Adresse |
| PTR | IP-Adresse zurück zu Hostname |
| SPF (TXT) | welche Server Mails für die Domain senden dürfen |

## Typisches Zusammenspiel
### Beispiel
Domain: `firma.de`

1. Empfänger-System fragt den **MX-Record** von `firma.de` ab.
2. Ergebnis könnte sein: `mail.firma.de`
3. Dann wird `mail.firma.de` über **A** oder **AAAA** in eine IP aufgelöst.
4. Für Vertrauensprüfungen kann zusätzlich **PTR** und **SPF** relevant sein.

## Warum PTR und SPF wichtig sind
| Record | Warum relevant? |
|---|---|
| PTR | fehlender Reverse DNS wirkt unseriös und spamverdächtig |
| SPF | verhindert bzw. erschwert Mail-Spoofing |

## Prüfungsfallen
| Irrtum | Korrektur |
|---|---|
| MX enthält direkt immer die IP-Adresse | nein, meist den Mailserver-Hostname |
| A-Record ersetzt MX | nein, A zeigt nur die IP eines Hosts |
| SPF ist für den Empfangsserver zuständig | SPF regelt, wer senden darf |

## Beispielaufgabe mit Lösung
**Aufgabe:** Warum reicht ein A-Record allein oft nicht aus, damit E-Mails für `firma.de` sauber zugestellt werden können?

**Lösung:**
Weil der sendende Mailserver wissen muss, **welcher Mailserver zuständig ist**, nicht nur welche IP irgendein Host hat.

**Begründung:**
Diese Information liefert der **MX-Record**. Erst danach werden A- oder AAAA-Einträge zur eigentlichen Erreichbarkeit benötigt.

## Typische Prüfungsszenarien
- MX, A, AAAA und PTR unterscheiden.
- Mailfluss über DNS grob erklären.
- SPF als Schutz gegen Spoofing einordnen.
- erklären, warum falsche DNS-Einträge Mailprobleme verursachen.

## Merksätze
- MX sagt "wer ist zuständig?".
- A/AAAA sagen "wie ist er erreichbar?".
- PTR und SPF helfen bei Vertrauenswürdigkeit und Spamvermeidung.
