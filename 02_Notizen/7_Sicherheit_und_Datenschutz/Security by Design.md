# Security by Design

## Definition
**Security by Design** bedeutet, dass Sicherheitsanforderungen von Anfang an in Systeme, Anwendungen und Prozesse eingebaut werden. **Privacy by Design** ergänzt dies um den datenschutzfreundlichen Entwurf.

## Warum ist das so?
Nachträglich eingebaute Sicherheit ist oft:
- teurer
- lückenhafter
- schwerer wartbar
- fachlich schlechter integriert

Wenn Sicherheit erst am Ende "daraufgesetzt" wird, entstehen leichter Schwachstellen und Fehlkonfigurationen.

## Zusammenspiel
- [[DSGVO und IT-Grundschutz (Personbezogene Daten usw..)]] fordert bei personenbezogenen Daten einen bewussten Umgang mit Schutzanforderungen.
- [[TOM]] setzt viele Designprinzipien praktisch um.
- [[Schutzbedafsanalyse und Riskoanalyse]] liefert die Bewertungsbasis.
- [[Berechtigungskonzepte]] und [[Zutritts-, Zugangs- und Zugriffskontrolle]] sind typische Umsetzungsfelder.

## Eigene Worte (prüfungsnah)
Security by Design heißt: Sicherheit ist kein Zusatzmodul, sondern Teil der Architektur. Man plant also schon beim Entwurf, wie Rechte, Segmentierung, sichere Standards und Fehlerszenarien behandelt werden.

## Wichtige Prinzipien
| Prinzip | Bedeutung |
|---|---|
| Least Privilege | nur die minimal nötigen Rechte vergeben |
| Defense in Depth | mehrere Schutzschichten kombinieren |
| Fail Secure | bei Fehlern in sicheren Zustand wechseln |
| Need to Know | Zugriff nur bei tatsächlichem Bedarf |
| Privacy by Default | datenschutzfreundliche Voreinstellungen |

## Typische Umsetzung
| Bereich | Beispiel |
|---|---|
| Benutzerrechte | Rollen statt Vollzugriff |
| Netzwerk | Segmentierung, Firewalls, getrennte Zonen |
| Anwendung | sichere Standardwerte, Eingabevalidierung |
| Betrieb | Logging, Härtung, Patchmanagement |
| Datenschutz | nur erforderliche Daten erheben |

## Security by Design vs. spätere Härtung
| Ansatz | Wirkung |
|---|---|
| Security by Design | Schutz von Anfang an eingeplant |
| nachträgliche Härtung | reagiert auf bereits bestehende Strukturen |

Beides kann nötig sein, aber Security by Design ist meist sauberer und wirtschaftlicher.

## Beispielaufgabe mit Lösung
**Aufgabe:** Eine Anwendung speichert standardmäßig alle Nutzerprofile öffentlich sichtbar und erlaubt jedem Benutzer Admin-Funktionen, bis diese manuell eingeschränkt werden. Welches Prinzip wird hier klar verletzt?

**Lösung:**
Vor allem **Privacy by Default** und **Least Privilege**.

**Begründung:**
Datenschutzfreundliche und sicherheitsarme Standardwerte müssten die Voreinstellung sein, nicht erst nachträglich aktiviert werden.

## Typische Prüfungsszenarien
- Security by Design in eigenen Worten erklären.
- Least Privilege und Defense in Depth nennen und anwenden.
- Privacy by Default von bloßer Datenschutzerklärung unterscheiden.
- begründen, warum spätere Absicherung oft teurer ist.

## Merksätze
- Gute Sicherheit wird geplant, nicht improvisiert.
- Standardwerte sollten sicher und datensparsam sein.
- Mehrere Schutzschichten sind robuster als eine einzige Maßnahme.
