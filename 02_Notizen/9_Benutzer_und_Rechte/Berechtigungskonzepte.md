# Berechtigungskonzepte

## Definition
**Berechtigungskonzepte** regeln, welche Benutzer, Gruppen oder Prozesse auf welche Ressourcen zugreifen dürfen und in welcher Form, zum Beispiel lesen, schreiben, ändern oder ausführen.

## Warum ist das so?
Nicht jeder Benutzer darf alles sehen oder ändern. Ohne Berechtigungskonzept entstehen Risiken:
- Datenabfluss
- Manipulation
- ungewollte Löschung
- Verstöße gegen Datenschutz und Compliance

Ein gutes Berechtigungskonzept schützt also Vertraulichkeit und Integrität und reduziert Bedienfehler.

## Zusammenspiel
- [[Zutritts-, Zugangs- und Zugriffskontrolle]] ordnet Rechte der Zugriffsebene zu.
- [[Schutzziele der IT]] liefert die sicherheitstechnische Zielsetzung.
- [[Active Directory und LDAP]] setzt Gruppen und Rollen praktisch um.
- [[MFA, SSO, Passwortrichtlinien]] ergänzt die Anmeldung, ersetzt aber keine Rechtevergabe.

## Eigene Worte (prüfungsnah)
Berechtigungskonzepte beantworten die Frage: "Was darf ein bereits angemeldeter Benutzer konkret tun?" Sie steuern also nicht den Login selbst, sondern den erlaubten Handlungsspielraum im System.

## Grundprinzipien
| Prinzip | Bedeutung |
|---|---|
| Least Privilege | nur die minimal nötigen Rechte vergeben |
| Need to Know | Zugriff nur auf benötigte Informationen |
| Trennung von Aufgaben | kritische Aufgaben auf mehrere Rollen verteilen |

## Wichtige Modelle
| Modell | Bedeutung | Typischer Einsatz |
|---|---|---|
| DAC | Eigentümer vergibt Rechte selbst | Dateisysteme, klassische Benutzerrechte |
| MAC | zentrale Sicherheitsstufen | Hochsicherheits- oder Spezialumgebungen |
| RBAC | Rechte an Rollen statt direkt an Benutzer | Unternehmen, AD-Gruppen, Fachrollen |

## Warum RBAC in Unternehmen oft sinnvoll ist
Statt 100 Benutzern einzeln Rechte zu geben, vergibt man Rechte an Rollen wie:
- Buchhaltung
- Personal
- Azubi
- Administrator

Benutzer erhalten dann nur die passende Rolle.

## Typische Beispiele
| Situation | passender Gedanke |
|---|---|
| Mitarbeiter darf nur eigene Abteilungsdaten sehen | Need to Know |
| Auszubildende sollen keine Adminrechte bekommen | Least Privilege |
| Rechte an Rolle "Buchhaltung" statt an einzelne Personen | RBAC |

## Beispielaufgabe mit Lösung
**Aufgabe:** Ein Unternehmen möchte Dateirechte nicht jedem einzelnen Benutzer direkt zuweisen, sondern über feste Rollen wie "Vertrieb" oder "Personal". Welches Modell passt am besten?

**Lösung:**
**RBAC (Role-Based Access Control)**

**Begründung:**
Rechte werden an Rollen gebunden und Benutzer erhalten die passende Rolle. Das ist wartbarer und übersichtlicher als Einzelzuweisungen.

## Typische Prüfungsszenarien
- Authentifizierung und Autorisierung abgrenzen.
- DAC, MAC und RBAC unterscheiden.
- Least Privilege und Need to Know erklären.
- RBAC als Standard in Unternehmensumgebungen einordnen.

## Merksätze
- Rechte folgen idealerweise Rollen, nicht Einzelpersonen.
- Least Privilege reduziert Schäden und Fehler.
- Anmeldung ist nicht gleich Berechtigung.
