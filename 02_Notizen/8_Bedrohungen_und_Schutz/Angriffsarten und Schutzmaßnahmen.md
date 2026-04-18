# Angriffsarten und Schutzmaßnahmen

## Definition
**Angriffsarten** sind typische Vorgehensweisen, mit denen Angreifer Daten, Systeme oder Benutzer kompromittieren wollen. **Schutzmaßnahmen** sind technische oder organisatorische Gegenmittel, um solche Angriffe zu verhindern, zu erschweren oder ihre Auswirkungen zu begrenzen.

## Warum ist das so?
IT-Sicherheit ist nicht abstrakt, sondern reagiert auf reale Bedrohungen:
- Menschen werden getäuscht
- Schwachstellen werden ausgenutzt
- Systeme werden überlastet
- Daten werden gestohlen, manipuliert oder verschlüsselt

Nur wenn man Angriffsarten versteht, kann man passende Schutzmaßnahmen auswählen.

## Zusammenspiel
- [[Schutzziele der IT]] hilft, Angriffe den betroffenen Sicherheitszielen zuzuordnen.
- [[Schutzbedafsanalyse und Riskoanalyse]] bewertet die Relevanz und Folgen.
- [[TOM]] liefert den Rahmen für Maßnahmen.
- [[Firewall (IDS, IPS, DMZ, ACL, Filtertabelle)]] und [[Zutritts-, Zugangs- und Zugriffskontrolle]] sind klassische Schutzbausteine.
- [[Verschlüsselung (Arten, Symmetrisch, Asymmetrisch, Hybride)]], [[Hashverfahren & digitale Signaturen]] und [[Zertifikate]] schützen vor bestimmten Manipulations- und Mitleseangriffen.

## Eigene Worte (prüfungsnah)
Angriffe unterscheiden sich nicht nur technisch, sondern auch in ihrem Ziel. Manche wollen Zugangsdaten stehlen, andere Systeme lahmlegen oder Daten manipulieren. Gute Schutzmaßnahmen passen deshalb zum konkreten Angriff und nicht nur allgemein zur "IT-Sicherheit".

## Wichtige Angriffsarten
| Angriff | Ziel / Wirkung | Typische Gegenmaßnahmen |
|---|---|---|
| Phishing / Social Engineering | Zugangsdaten oder Handlung erzwingen | Schulung, MFA, Sensibilisierung |
| Ransomware | Daten verschlüsseln, Verfügbarkeit zerstören | Backups, Segmentierung, Rechtebegrenzung |
| DDoS | Dienste überlasten | Rate Limiting, Provider-Schutz, Load Balancing |
| SQL-Injection | Datenbank manipulieren oder auslesen | Prepared Statements, Validierung, WAF |
| Man-in-the-Middle | Daten mitlesen oder verändern | TLS, Zertifikatsprüfung, sichere Netze |
| Brute Force | Passwörter erraten | MFA, Kontosperre, starke Passwörter |
| Malware allgemein | Systeme kompromittieren | Updates, AV/EDR, Schulung, Rechtebegrenzung |

## Angriffe und Schutzziele
| Angriff | besonders betroffenes Schutzziel |
|---|---|
| Phishing | Vertraulichkeit, oft auch Integrität |
| Ransomware | Verfügbarkeit, oft auch Integrität |
| DDoS | Verfügbarkeit |
| SQL-Injection | Integrität und Vertraulichkeit |
| MitM | Vertraulichkeit und Integrität |
| Brute Force | Zugangskontrolle / Vertraulichkeit |

## Typische Schutzlogik
### Organisatorisch
- Awareness-Schulungen
- klare Prozesse
- Berechtigungskonzepte
- Notfallplanung

### Technisch
- MFA
- Segmentierung
- Verschlüsselung
- Backups
- Firewalls / IDS / IPS

## Beispielaufgabe mit Lösung
**Aufgabe:** Ein Unternehmen wird Opfer einer Ransomware-Attacke. Welche Maßnahme reduziert den Schaden am zuverlässigsten, wenn die Systeme bereits verschlüsselt wurden?

**Lösung:**
Saubere, getrennte **Backups**.

**Begründung:**
1. Ransomware zerstört vor allem die Verfügbarkeit.
2. Wenn produktive Daten verschlüsselt sind, braucht man eine unveränderte Wiederherstellungsbasis.
3. Backups müssen geschützt und idealerweise nicht direkt durch die Schadsoftware erreichbar sein.

## Typische Prüfungsszenarien
- Angriffe passenden Schutzzielen zuordnen.
- zu einem Angriff sinnvolle Maßnahmen nennen.
- organisatorische und technische Maßnahmen mischen.
- erklären, warum MFA gegen Phishing und Brute Force hilft, aber nicht alles löst.

## Merksätze
- Nicht jeder Angriff ist rein technisch, oft ist der Mensch das Ziel.
- Maßnahmen müssen zur Angriffsart passen.
- Viele Angriffe verletzen mehrere Schutzziele gleichzeitig.
