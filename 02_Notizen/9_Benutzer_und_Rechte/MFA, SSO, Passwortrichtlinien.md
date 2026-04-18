# MFA, SSO, Passwortrichtlinien

## Definition
Diese Konzepte gehören zur modernen Authentifizierung:
- **MFA (Multi-Faktor-Authentifizierung)**: Anmeldung mit mindestens zwei unterschiedlichen Faktoren
- **SSO (Single Sign-On)**: einmal anmelden, mehrere Dienste nutzen
- **Passwortrichtlinien**: Regeln für sichere Passwortverwendung

## Warum ist das so?
Passwörter allein sind oft zu schwach:
- sie werden wiederverwendet
- sie werden erraten
- sie werden geleakt oder per Phishing gestohlen

Darum braucht man zusätzliche Schutzmechanismen und saubere Richtlinien.

## Zusammenspiel
- [[Active Directory und LDAP]] setzt viele dieser Konzepte in Unternehmensumgebungen um.
- [[Berechtigungskonzepte]] regelt danach, was Benutzer überhaupt dürfen.
- [[RADIUS und AAA]] nutzt Authentifizierung oft zentral weiter.
- [[Zutritts-, Zugangs- und Zugriffskontrolle]] ordnet MFA vor allem der Zugangskontrolle zu.

## Eigene Worte (prüfungsnah)
MFA stärkt die Anmeldung, SSO vereinfacht die Nutzung mehrerer Dienste und Passwortrichtlinien verbessern die Grundsicherheit von Kennwörtern. Das sind also verwandte, aber unterschiedliche Bausteine.

## MFA
| Faktorart | Beispiel |
|---|---|
| Wissen | Passwort, PIN |
| Besitz | Smartphone, Hardware-Token, Smartcard |
| Sein | Fingerabdruck, Gesicht |

**Wichtig:** Zwei Passwörter sind **keine** MFA, weil sie aus derselben Faktorenklasse stammen.

## SSO
SSO bedeutet:
- einmal authentifizieren
- mehrere verbundene Dienste nutzen
- nicht an jedem System erneut separat anmelden

Typische Technologien:
- Kerberos
- SAML
- OAuth2 / OpenID Connect

## Passwortrichtlinien
| Regel | Zweck |
|---|---|
| Mindestlänge | erschwert Erraten |
| Komplexitätsanforderung | erhöht Variantenvielfalt |
| Passwort-Historie | verhindert Wiederverwendung |
| Sperrschwelle | schützt gegen Brute Force |
| Gültigkeitsregeln | steuern Lebensdauer und Erneuerung |

## MFA vs. SSO
| Frage | MFA | SSO |
|---|---|---|
| erhöht Sicherheit der Anmeldung? | ja | nicht automatisch |
| verbessert Nutzerkomfort? | teils | stark |
| reduziert Passwortanzahl? | nein | oft ja |

**Merke:** SSO macht Anmeldung bequemer, MFA macht Anmeldung sicherer.

## Beispielaufgabe mit Lösung
**Aufgabe:** Ein Benutzer meldet sich morgens einmal an und kann danach E-Mail, Intranet und Ticketsystem ohne weitere Logins nutzen. Welches Konzept beschreibt das am besten?

**Lösung:**
**SSO**

**Begründung:**
Der Benutzer authentifiziert sich einmal und nutzt danach mehrere verbundene Systeme ohne erneute Anmeldung.

## Typische Prüfungsszenarien
- MFA und SSO unterscheiden.
- Faktorenklassen korrekt zuordnen.
- erklären, warum zwei Wissensfaktoren keine MFA sind.
- Passwortrichtlinien als Schutz gegen Brute Force und schlechte Kennwörter erklären.

## Merksätze
- MFA = mehrere Faktorarten.
- SSO = einmal anmelden, mehrfach nutzen.
- SSO ersetzt MFA nicht.
