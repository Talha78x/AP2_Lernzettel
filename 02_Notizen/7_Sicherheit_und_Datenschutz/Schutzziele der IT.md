# Schutzziele der IT

## Definition
Die grundlegenden Schutzziele der Informationssicherheit sind:
- **Vertraulichkeit**
- **Integrität**
- **Verfügbarkeit**

Zusammen werden sie oft als **CIA-Triade** bezeichnet.

## Warum ist das so?
IT-Sicherheit braucht klare Ziele, sonst bleibt unklar, was eigentlich geschützt werden soll. Die Schutzziele beantworten:
- Wer darf Daten sehen?
- Dürfen Daten unbemerkt verändert werden?
- Sind Systeme und Daten nutzbar, wenn sie gebraucht werden?

## Zusammenspiel
- [[Schutzbedafsanalyse und Riskoanalyse]] bewertet Systeme anhand dieser Ziele.
- [[TOM]] setzt Maßnahmen um, die die Ziele absichern.
- [[DSGVO und IT-Grundschutz (Personbezogene Daten usw..)]] verlangt insbesondere bei personenbezogenen Daten geeigneten Schutz.
- [[Angriffsarten und Schutzmaßnahmen]] zeigt typische Verletzungen dieser Ziele.
- [[Hashverfahren & digitale Signaturen]] und [[Verschlüsselung (Arten, Symmetrisch, Asymmetrisch, Hybride)]] sind typische Maßnahmen für Integrität und Vertraulichkeit.

## Eigene Worte (prüfungsnah)
Die drei Schutzziele sind die Grundfragen der IT-Sicherheit: Bleiben Daten geheim? Bleiben sie korrekt? Bleiben sie verfügbar? Fast jede Prüfungsaufgabe im Sicherheitsbereich lässt sich auf eines oder mehrere dieser Ziele zurückführen.

## Die drei Kernziele
| Schutzziel | Bedeutung | Typische Bedrohung | Typische Maßnahme |
|---|---|---|---|
| Vertraulichkeit | nur Berechtigte dürfen lesen | Sniffing, Datenleck | Verschlüsselung, Rechte, MFA |
| Integrität | Daten bleiben korrekt und unverändert | Manipulation, Injection | Hashwerte, Signaturen, Berechtigungen |
| Verfügbarkeit | Systeme und Daten sind nutzbar | DDoS, Ausfall, Ransomware | Redundanz, Backup, USV |

## Erweiterte Schutzziele
| Ziel | Bedeutung |
|---|---|
| Authentizität | Ist jemand oder etwas wirklich echt? |
| Verbindlichkeit / Nichtabstreitbarkeit | kann eine Handlung später nicht abgestritten werden |

Diese ergänzen die CIA-Triade, ersetzen sie aber nicht.

## Typische Zuordnungen
| Situation | betroffenes Schutzziel |
|---|---|
| E-Mail wird mitgelesen | Vertraulichkeit |
| Übertragene Daten werden verändert | Integrität |
| Server ist durch Angriff nicht erreichbar | Verfügbarkeit |
| Benutzer gibt sich als anderer aus | Authentizität |

## Beispielaufgabe mit Lösung
**Aufgabe:** Ein Angreifer verändert unbemerkt eine Konfigurationsdatei auf einem Server. Welches Schutzziel ist in erster Linie verletzt?

**Lösung:**
**Integrität**

**Begründung:**
Die Datei ist nicht mehr korrekt bzw. unverändert. Es geht hier primär nicht um Geheimhaltung, sondern um die Unverändertheit der Daten.

## Typische Prüfungsszenarien
- Angriffe einem Schutzziel zuordnen.
- Maßnahmen einem Schutzziel zuordnen.
- CIA-Triade erklären.
- Integrität und Vertraulichkeit voneinander abgrenzen.

## Merksätze
- Vertraulichkeit = geheim.
- Integrität = korrekt und unverändert.
- Verfügbarkeit = nutzbar zur richtigen Zeit.
- Viele reale Angriffe verletzen mehr als ein Schutzziel gleichzeitig.
