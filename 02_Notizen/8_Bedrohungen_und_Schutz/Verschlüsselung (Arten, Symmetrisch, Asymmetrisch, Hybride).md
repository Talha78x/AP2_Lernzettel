# Verschlüsselung (Arten, Symmetrisch, Asymmetrisch, Hybride)

## Definition
**Verschlüsselung** wandelt Klartext in unlesbaren Geheimtext um, damit nur berechtigte Parteien die Informationen lesen können. Hauptziel ist die **Vertraulichkeit**.

## Warum ist das so?
Daten werden gespeichert, übertragen und verarbeitet. Ohne Verschlüsselung könnten sie:
- mitgelesen werden
- gestohlen werden
- an unsicheren Orten offengelegt werden

Deshalb braucht man Verfahren, die Daten nur für berechtigte Empfänger lesbar machen.

## Zusammenspiel
- [[Schutzziele der IT]] ordnet Verschlüsselung vor allem der Vertraulichkeit zu.
- [[Hashverfahren & digitale Signaturen]] ergänzt Integrität und Authentizität.
- [[Zertifikate]] helfen beim sicheren Umgang mit öffentlichen Schlüsseln.
- [[TLS & SSL]] ist ein typisches Beispiel für hybride Verschlüsselung.
- [[VPN (Tunneling, standortübergreifende Kommunikation)]] nutzt Verschlüsselung zur Absicherung ganzer Verbindungen.

## Eigene Worte (prüfungsnah)
Verschlüsselung macht Daten für Unbefugte unlesbar. Dabei gibt es schnelle Verfahren mit gemeinsamem Schlüssel, aufwendigere Verfahren mit Schlüsselpaaren und Mischformen, die beide Vorteile kombinieren.

## Symmetrische Verschlüsselung
| Merkmal | Erklärung |
|---|---|
| Schlüssel | derselbe Schlüssel für Ver- und Entschlüsselung |
| Vorteil | sehr schnell |
| Nachteil | sicherer Schlüsselaustausch ist schwierig |
| Beispiel | AES |

## Asymmetrische Verschlüsselung
| Merkmal | Erklärung |
|---|---|
| Schlüssel | Public Key und Private Key |
| Vorteil | Public Key darf verteilt werden |
| Nachteil | deutlich langsamer |
| Beispiele | RSA, ECC |

## Hybride Verschlüsselung
Hier werden beide Verfahren kombiniert:
1. Ein symmetrischer Sitzungsschlüssel wird erzeugt.
2. Die eigentlichen Nutzdaten werden schnell symmetrisch verschlüsselt.
3. Der Sitzungsschlüssel wird asymmetrisch geschützt übertragen.

So arbeitet zum Beispiel **TLS**.

## Vergleich
| Verfahren | Stärke | Schwäche | Typischer Einsatz |
|---|---|---|---|
| symmetrisch | schnell | Schlüsselaustauschproblem | Festplatten, große Datenmengen |
| asymmetrisch | Schlüsselverteilung einfacher | langsam | Schlüsselaustausch, Signaturen |
| hybrid | kombiniert Vorteile | komplexer | TLS, moderne sichere Kommunikation |

## Typische Prüfungsfallen
| Irrtum | Korrektur |
|---|---|
| asymmetrisch ist immer besser | nein, aber für große Datenmengen zu langsam |
| symmetrisch braucht zwei verschiedene Schlüssel | nein, denselben |
| Verschlüsselung beweist automatisch den Absender | nein, dafür braucht man oft Signaturen/Zertifikate |

## Beispielaufgabe mit Lösung
**Aufgabe:** Warum wird bei TLS nicht die komplette Datenübertragung rein asymmetrisch verschlüsselt?

**Lösung:**
Weil asymmetrische Verfahren für große Datenmengen zu langsam und rechenintensiv sind.

**Begründung:**
TLS nutzt daher einen hybriden Ansatz: asymmetrisch für den sicheren Austausch des Sitzungsschlüssels, symmetrisch für die eigentlichen Nutzdaten.

## Typische Prüfungsszenarien
- symmetrisch, asymmetrisch und hybrid unterscheiden.
- Schlüsselaustauschproblem erklären.
- TLS als hybrides Verfahren einordnen.
- Verschlüsselung von Signatur und Hashing abgrenzen.

## Merksätze
- Symmetrisch ist schnell, asymmetrisch ist flexibel.
- Hybrid verbindet die Stärken beider Verfahren.
- Verschlüsselung schützt vor allem Vertraulichkeit, nicht automatisch Integrität oder Authentizität.
