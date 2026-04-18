# Hashverfahren & digitale Signaturen

## Definition
**Hashverfahren** berechnen aus Daten einen eindeutigen Prüfwert fester Länge. **Digitale Signaturen** nutzen Hashwerte und asymmetrische Kryptografie, um Authentizität und Integrität nachzuweisen.

## Warum ist das so?
In der IT reicht es oft nicht, Daten nur geheim zu halten. Man muss auch prüfen können:
- wurden Daten verändert?
- stammt ein Dokument wirklich vom angegebenen Absender?

Hashwerte und digitale Signaturen lösen genau diese beiden Fragen.

## Zusammenspiel
- [[Schutzziele der IT]] ordnet Hashing und Signaturen vor allem Integrität und Authentizität zu.
- [[Verschlüsselung (Arten, Symmetrisch, Asymmetrisch, Hybride)]] liefert die asymmetrische Grundlage der Signatur.
- [[Zertifikate]] sorgen dafür, dass der öffentliche Schlüssel einer Identität zugeordnet werden kann.
- [[TLS & SSL]] und viele PKI-Verfahren nutzen genau dieses Zusammenspiel.

## Eigene Worte (prüfungsnah)
Ein Hash ist wie ein digitaler Fingerabdruck der Daten. Eine digitale Signatur ist vereinfacht gesagt ein signierter Hash, mit dem man prüfen kann, ob die Daten unverändert sind und vom behaupteten Absender stammen.

## Hashverfahren
| Eigenschaft | Bedeutung |
|---|---|
| feste Länge | egal wie groß die Eingabe ist, der Hash hat definierte Länge |
| Einwegfunktion | aus dem Hash soll die Ursprungsnachricht nicht berechenbar sein |
| Lawineneffekt | kleine Änderungen erzeugen stark anderen Hash |
| Kollisionsarmut | unterschiedliche Daten sollen nicht denselben Hash ergeben |

## Typische Einsätze von Hashverfahren
| Einsatz | Zweck |
|---|---|
| Passwortspeicherung | kein Klartext im System |
| Prüfsummen von Downloads | Integrität prüfen |
| digitale Signaturen | Nachricht vor dem Signieren verdichten |

**Wichtig:** Hashing ist **keine Verschlüsselung**.

## Digitale Signatur: Ablauf
1. Der Absender berechnet den Hash des Dokuments.
2. Dieser Hash wird mit dem **privaten Schlüssel** des Absenders signiert.
3. Der Empfänger entschlüsselt bzw. prüft die Signatur mit dem **öffentlichen Schlüssel**.
4. Der Empfänger berechnet zusätzlich selbst den Hash des empfangenen Dokuments.
5. Stimmen beide Hashwerte überein, ist das Dokument unverändert und die Signatur passt.

## Was beweist eine digitale Signatur?
| Aussage | Warum? |
|---|---|
| Integrität | jede Änderung verändert den Hash |
| Authentizität | Signatur passt nur zum korrekten Schlüsselpaar |
| Nichtabstreitbarkeit | der Besitzer des privaten Schlüssels hat signiert |

## Typische Prüfungsfallen
| Irrtum | Korrektur |
|---|---|
| Hash = Verschlüsselung | nein, ein Hash ist nicht zur Rückumwandlung gedacht |
| Signatur = Geheimhaltung | nein, Signatur schützt Authentizität/Integrität |
| Signieren mit Public Key | falsch, signiert wird mit Private Key |

## Beispielaufgabe mit Lösung
**Aufgabe:** Ein Empfänger möchte prüfen, ob ein signiertes PDF unverändert ist und wirklich vom Absender stammt. Welche zwei Schritte sind dafür zentral?

**Lösung:**
1. Signatur mit dem **öffentlichen Schlüssel** des Absenders prüfen.
2. Eigenen Hash des PDFs bilden und mit dem aus der Signatur abgeleiteten Wert vergleichen.

**Begründung:**
So werden sowohl die Echtheit der Signatur als auch die Unverändertheit des Inhalts überprüft.

## Typische Prüfungsszenarien
- Hashing von Verschlüsselung unterscheiden.
- Ablauf einer digitalen Signatur erklären.
- privater und öffentlicher Schlüssel korrekt zuordnen.
- Integrität und Authentizität an Signaturen erklären.

## Merksätze
- Hash = Fingerabdruck.
- Signatur = signierter Hash.
- Signatur schützt nicht die Geheimhaltung, sondern Echtheit und Unverändertheit.
