# Active Directory und LDAP

## Definition
**Active Directory (AD)** ist Microsofts zentraler Verzeichnisdienst für Windows-Domänen. Er verwaltet Benutzer, Computer, Gruppen, Richtlinien und weitere Objekte einer Domänenumgebung.

**LDAP (Lightweight Directory Access Protocol)** ist ein Protokoll, mit dem auf Verzeichnisdienste zugegriffen wird. LDAP ist also nicht dasselbe wie AD, sondern eine "Sprache", über die ein Verzeichnisdienst angesprochen werden kann.

## Warum ist das so?
In Unternehmen müssen Benutzerkonten, Geräte, Gruppen und Rechte zentral verwaltet werden. Ohne zentrale Verwaltung würden schnell Probleme entstehen:
- uneinheitliche Benutzerkonten
- hoher Administrationsaufwand
- schlechte Skalierbarkeit
- unsaubere Rechtevergabe

Ein Verzeichnisdienst bündelt diese Informationen an einer zentralen Stelle.

## Zusammenspiel
- [[Domänenkonzepte]] erweitert die Struktur um Forests, Trees, Sites und Replikation.
- [[Berechtigungskonzepte]] nutzt Gruppen und Rollen aus dem AD.
- [[MFA, SSO, Passwortrichtlinien]] ergänzt Authentifizierung und Richtlinien.
- [[RADIUS und AAA]] kann Benutzer gegen AD-Verzeichnisse prüfen.
- [[Netzwerkrelevante Dienste (DHCP, DNS, NTP, SNMP...)]] ist wichtig, weil AD stark auf DNS und Zeitkonsistenz angewiesen ist.

## Eigene Worte (prüfungsnah)
Active Directory ist die zentrale Benutzer- und Rechnerverwaltung in Windows-Umgebungen. LDAP ist das Zugriffsprotokoll auf solche Verzeichnisdaten. AD ist also das Verzeichnis, LDAP ist ein Weg, damit zu arbeiten.

## Wichtige AD-Bausteine
| Begriff | Bedeutung |
|---|---|
| Domäne | grundlegender Verwaltungsbereich |
| Domänencontroller (DC) | Server, der AD-Dienste bereitstellt |
| OU (Organizational Unit) | logische Gliederung von Objekten |
| GPO (Group Policy Object) | zentrale Richtlinien für Benutzer und Computer |
| Gruppe | Bündelung von Benutzern oder Rechten |

## AD und LDAP unterscheiden
| Frage | Active Directory | LDAP |
|---|---|---|
| Was ist es? | Verzeichnisdienst | Zugriffsprotokoll |
| Aufgabe | Objekte zentral verwalten | Verzeichnisdaten abfragen/ändern |
| Beispiel | Benutzer im AD anlegen | Benutzer per LDAP abfragen |

## OU und GPO im Zusammenspiel
**OU:** dient zur logischen Strukturierung, zum Beispiel:
- `Mitarbeiter`
- `Server`
- `Azubis`

**GPO:** wirkt auf Benutzer oder Computer in einer OU, zum Beispiel:
- Passwortregeln
- Desktoprichtlinien
- Softwareverteilung

## Beispielaufgabe mit Lösung
**Aufgabe:** Ein Unternehmen möchte Benutzerkonten, Computerobjekte und zentrale Richtlinien wie Passwortvorgaben in einer Windows-Umgebung verwalten. Welche Lösung ist passend?

**Lösung:**
**Active Directory**

**Begründung:**
AD ist der zentrale Verzeichnisdienst für genau diese Objekte und Richtlinien. LDAP wäre dabei das Protokoll für den Zugriff auf Verzeichnisinformationen, nicht die eigentliche Verwaltungsplattform selbst.

## Typische Prüfungsszenarien
- AD und LDAP unterscheiden.
- Aufgabe eines Domänencontrollers erklären.
- OUs und GPOs korrekt einordnen.
- zentrale Benutzerverwaltung als Vorteil nennen.

## Merksätze
- AD ist der Verzeichnisdienst, LDAP ist das Protokoll.
- Domänencontroller stellen AD-Dienste bereit.
- OUs strukturieren, GPOs steuern.
