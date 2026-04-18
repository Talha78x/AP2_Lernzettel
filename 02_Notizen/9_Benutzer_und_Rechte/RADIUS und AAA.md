# RADIUS und AAA

## Definition
**AAA** steht für:
- **Authentication**: Wer bist du?
- **Authorization**: Was darfst du?
- **Accounting**: Was wurde wann genutzt oder getan?

**RADIUS (Remote Authentication Dial-In User Service)** ist ein verbreitetes Protokoll zur zentralen Umsetzung von AAA, besonders im Netzwerkzugang.

## Warum ist das so?
Gerade bei WLAN, VPN oder Netzwerkinfrastruktur soll der Zugang nicht lokal auf jedem Gerät einzeln verwaltet werden. Es braucht:
- zentrale Benutzerprüfung
- zentrale Rechteentscheidung
- nachvollziehbare Protokollierung

AAA und RADIUS schaffen dafür eine gemeinsame Struktur.

## Zusammenspiel
- [[Active Directory und LDAP]] liefert oft die Benutzerbasis im Hintergrund.
- [[MFA, SSO, Passwortrichtlinien]] ergänzt die Authentifizierung.
- [[Firewall (IDS, IPS, DMZ, ACL, Filtertabelle)]] und Netzwerkkomponenten setzen Entscheidungen praktisch durch.
- [[Zutritts-, Zugangs- und Zugriffskontrolle]] ordnet AAA vor allem Zugang und teilweise Zugriff zu.

## Eigene Worte (prüfungsnah)
AAA beschreibt drei Fragen gleichzeitig: Wer bist du, was darfst du und was wurde protokolliert? RADIUS ist ein technischer Dienst, mit dem diese Prüfungen zentral für Netzwerkzugänge umgesetzt werden können.

## AAA im Überblick
| Teil | Frage | Beispiel |
|---|---|---|
| Authentication | Wer bist du? | Login mit Benutzername, Zertifikat oder Passwort |
| Authorization | Was darfst du? | Zugriff auf VLAN, WLAN oder VPN erlauben |
| Accounting | Was wurde genutzt? | Login-Zeit, Sitzungsdauer, Verbindungsdaten protokollieren |

## RADIUS
Typische Nutzung:
- WLAN mit 802.1X
- VPN-Zugänge
- Switch- oder Administrationszugänge

**Typische Ports:** UDP 1812/1813

## Beispielhafter Ablauf
1. Ein Benutzer verbindet sich mit einem WLAN.
2. Access Point oder Controller leitet die Anfrage an den RADIUS-Server weiter.
3. Der RADIUS-Server prüft Identität und Richtlinien.
4. Zugriff wird erlaubt oder verweigert.
5. Optional werden Sitzungsdaten protokolliert.

## RADIUS und AAA unterscheiden
| Begriff | Rolle |
|---|---|
| AAA | Konzept / Modell |
| RADIUS | technisches Protokoll zur Umsetzung |

## Beispielaufgabe mit Lösung
**Aufgabe:** Ein Unternehmen möchte zentrale Benutzerprüfung, VLAN-Zuweisung und Sitzungsprotokollierung für WLAN-Zugänge. Welches Modell beschreibt die Anforderungen und welches Protokoll setzt sie typischerweise um?

**Lösung:**
- Modell: **AAA**
- Protokoll: **RADIUS**

**Begründung:**
AAA beschreibt die drei fachlichen Bereiche. RADIUS ist das typische technische Protokoll, um diese zentral umzusetzen.

## Typische Prüfungsszenarien
- Authentifizierung und Autorisierung unterscheiden.
- AAA und RADIUS gegeneinander abgrenzen.
- typischen Einsatz von RADIUS im WLAN oder VPN erklären.
- Accounting richtig einordnen.

## Merksätze
- AAA ist das Modell, RADIUS ist oft die Umsetzung.
- Authentifizierung prüft Identität, Autorisierung prüft Rechte.
- Accounting ist Protokollierung, nicht Berechtigungsvergabe.
