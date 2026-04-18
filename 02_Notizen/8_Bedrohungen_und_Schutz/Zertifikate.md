# Zertifikate

## Definition
Ein **Zertifikat** ist ein digitaler Nachweis, dass ein bestimmter öffentlicher Schlüssel zu einer bestimmten Identität gehört, zum Beispiel:
- einer Domain
- einem Server
- einer Person
- einer Organisation

## Warum ist das so?
Ein öffentlicher Schlüssel allein sagt noch nicht, wem er wirklich gehört. Ohne Vertrauensmechanismus könnte ein Angreifer einfach einen eigenen Schlüssel als "echten Serverschlüssel" ausgeben.

Zertifikate schaffen deshalb eine vertrauenswürdige Zuordnung zwischen Identität und Public Key.

## Zusammenspiel
- [[Verschlüsselung (Arten, Symmetrisch, Asymmetrisch, Hybride)]] liefert die Schlüsselbasis.
- [[Hashverfahren & digitale Signaturen]] erklärt, wie Zertifikate digital signiert werden.
- [[TLS & SSL]] nutzt Zertifikate zur Serverauthentifizierung.
- [[DSGVO und IT-Grundschutz (Personbezogene Daten usw..)]] und [[Security by Design]] profitieren von vertrauenswürdiger Kommunikation.

## Eigene Worte (prüfungsnah)
Ein Zertifikat ist wie ein digitaler Ausweis für einen öffentlichen Schlüssel. Es bestätigt nicht die ganze Sicherheit eines Systems, sondern vor allem: Dieser Public Key gehört zu genau dieser Identität und wurde von einer vertrauenswürdigen Stelle bestätigt.

## Typische Inhalte eines Zertifikats
| Bestandteil | Bedeutung |
|---|---|
| Inhaber / Subject | zu welcher Identität das Zertifikat gehört |
| Public Key | öffentlicher Schlüssel des Inhabers |
| Gültigkeitszeitraum | von wann bis wann das Zertifikat gültig ist |
| Aussteller / Issuer | welche Zertifizierungsstelle es ausgestellt hat |
| Signatur der CA | Nachweis der Vertrauensbeziehung |

## PKI und Vertrauenskette
Eine **PKI (Public Key Infrastructure)** umfasst:
- Root CA
- Zwischenzertifizierungsstellen
- Endzertifikate
- Prüf- und Widerrufsmechanismen

| Bestandteil | Aufgabe |
|---|---|
| Root CA | oberste Vertrauensinstanz |
| Intermediate / Sub CA | stellt Endzertifikate im Auftrag aus |
| Endzertifikat | Zertifikat für Server, Benutzer oder Dienst |

## Warum vertraut man einem Serverzertifikat?
Weil die Vertrauenskette geprüft wird:
1. Das Serverzertifikat ist von einer CA signiert.
2. Diese CA ist selbst durch eine vertrauenswürdige übergeordnete CA eingebunden.
3. Am Ende steht eine Root CA, die im System oder Browser als vertrauenswürdig hinterlegt ist.

## Widerruf und Gültigkeit
Ein Zertifikat kann ungültig sein, obwohl das Enddatum noch nicht erreicht ist, zum Beispiel:
- Private Key kompromittiert
- falsche Ausstellung
- Zertifikat ersetzt

Typische Prüfmechanismen:
- **CRL** (Certificate Revocation List)
- **OCSP**

## Typische Prüfungsfallen
| Irrtum | Korrektur |
|---|---|
| Zertifikat = privater Schlüssel | falsch, der private Schlüssel bleibt geheim |
| Zertifikat verschlüsselt die Daten selbst | falsch, es bestätigt Identität und Public Key |
| Gültiges Zertifikat heißt automatisch sicheres System | nein, es ist nur ein Baustein |

## Beispielaufgabe mit Lösung
**Aufgabe:** Warum warnt ein Browser, wenn das Zertifikat einer Webseite abgelaufen ist?

**Lösung:**
Weil die Vertrauensprüfung fehlschlägt.

**Begründung:**
Ein Zertifikat ist nur innerhalb seines Gültigkeitszeitraums vertrauenswürdig. Ist es abgelaufen, kann die Identität des Gegenübers nicht mehr regelkonform bestätigt werden.

## Typische Prüfungsszenarien
- Zertifikat, Public Key und Private Key unterscheiden.
- PKI und Vertrauenskette erklären.
- Root CA und Intermediate CA einordnen.
- Gründe für Zertifikatswarnungen nennen.

## Merksätze
- Ein Zertifikat bestätigt einen öffentlichen Schlüssel.
- Der private Schlüssel gehört nicht ins Zertifikat.
- Vertrauen entsteht über die Zertifikatskette, nicht durch den Schlüssel allein.
