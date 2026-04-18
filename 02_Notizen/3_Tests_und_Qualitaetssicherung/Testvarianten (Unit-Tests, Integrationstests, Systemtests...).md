# Testvarianten (Unit-Tests, Integrationstests, Systemtests...)

## Definition
Testvarianten beschreiben, **auf welcher Ebene** ein System geprüft wird. Dabei wird vom kleinen, isolierten Baustein bis zum kompletten Gesamtsystem getestet.

Die wichtigsten Varianten sind:
- **Unit-Test**
- **Integrationstest**
- **Systemtest**
- **Akzeptanztest**

## Warum ist das so?
Fehler entstehen auf unterschiedlichen Ebenen:
- innerhalb einer einzelnen Funktion
- an Schnittstellen zwischen Komponenten
- im Gesamtsystem unter realen Bedingungen
- bei der fachlichen Abnahme durch den Auftraggeber

Ein einziger Testtyp reicht deshalb nicht aus. Viele kleine Tests finden technische Fehler früh, größere Tests prüfen das Zusammenspiel.

## Zusammenspiel
- [[Statische und dynamischen Testverfahren]] klärt, ob ein Test ohne oder mit Ausführung erfolgt.
- [[Debugging]] setzt häufig dort an, wo ein Test fehlschlägt.
- [[TDD, PDCA, KVP, Kennzahlen und Soll-Ist-Vergleich]] arbeitet vor allem mit Unit-Tests im Entwicklungsalltag.
- [[APIs und REST]] und [[Relationale, nicht relationale & NoSQL Datenbanken]] spielen oft in Integrations- und Systemtests hinein.
- [[Versionsmanagement (GIT, Repos) des Quellcodes]] bindet diese Tests häufig in Build- und Deployment-Prozesse ein.

## Eigene Worte (prüfungsnah)
Man kann sich die Testarten wie ein Gebäude vorstellen. Unit-Tests prüfen einzelne Bausteine, Integrationstests die Verbindungen zwischen den Bausteinen, Systemtests das ganze Gebäude und Akzeptanztests die Frage, ob der Auftraggeber das Gebäude so wollte.

## Die Testpyramide
| Ebene | Fokus | Vorteil | Nachteil |
|---|---|---|---|
| Unit-Tests | einzelne Funktion, Methode oder Klasse | schnell, günstig, präzise | prüfen kaum echtes Zusammenspiel |
| Integrationstests | Schnittstellen zwischen Modulen | Fehler in Datenfluss und Kommunikation sichtbar | langsamer, komplexer |
| Systemtests | vollständiges Gesamtsystem | realitätsnah | teuer und aufwendig |
| Akzeptanztests | fachliche Abnahme | prüft Kundennutzen | oft spät im Prozess |

## Testarten im Detail
### Unit-Tests
Ein Unit-Test prüft die kleinste testbare Einheit isoliert, zum Beispiel eine Funktion zur Rabattberechnung oder eine Methode zur Prüfung einer IPv4-Adresse.

**Typische Merkmale:**
- läuft schnell
- nutzt oft Mocks oder Stubs
- wird meist vom Entwickler geschrieben
- gut geeignet für TDD

### Integrationstests
Integrationstests prüfen, ob mehrere Bausteine korrekt zusammenarbeiten.

**Beispiele:**
- Webanwendung speichert Daten korrekt in der Datenbank
- API antwortet im richtigen Format
- Authentifizierung funktioniert mit LDAP oder Active Directory

### Systemtests
Beim Systemtest wird das komplette System in einer Umgebung geprüft, die der echten Nutzung möglichst nahekommt.

**Beispiele:**
- Login, Rollenprüfung, Datenanzeige und Reporting als durchgehender Ablauf
- Installation eines Systems mit realer Netzwerkanbindung

### Akzeptanztests
Hier prüft der Kunde, Fachbereich oder Product Owner, ob die Lösung die fachlichen Anforderungen erfüllt.

**Wichtig:** Technisch kann ein System korrekt laufen und trotzdem fachlich nicht akzeptabel sein.

## Beispielhafte Zuordnung
| Frage | Passende Testart |
|---|---|
| Liefert die Funktion `berechneRabatt()` den richtigen Wert? | Unit-Test |
| Kann die Web-App Bestellungen korrekt in MySQL speichern? | Integrationstest |
| Funktioniert der gesamte Bestellprozess vom Login bis zur Rechnung? | Systemtest |
| Entspricht der Ablauf den Anforderungen des Fachbereichs? | Akzeptanztest |

## Beispielaufgabe mit Lösung
**Aufgabe:** Ordne die folgenden Situationen zu:
1. Eine Methode `summe(a, b)` wird mit mehreren Eingaben geprüft.
2. Eine Anwendung wird mit echter Datenbank gestartet, um den Login zu testen.
3. Der Fachbereich überprüft, ob der neue Bestellablauf alle Anforderungen erfüllt.

**Lösung:**
1. **Unit-Test**, weil eine kleine isolierte Funktion geprüft wird.
2. **Integrationstest** oder **Systemtest**, je nach Umfang.
   Wenn nur das Zusammenspiel Anwendung plus Datenbank geprüft wird, ist es meist ein **Integrationstest**.
   Wenn der komplette Ablauf in realistischer Umgebung geprüft wird, eher **Systemtest**.
3. **Akzeptanztest**, weil die fachliche Abnahme im Vordergrund steht.

## Typische Prüfungsszenarien
- Testarten voneinander abgrenzen.
- Beispiele richtig zuordnen.
- Vorteile vieler Unit-Tests erklären.
- Warum Integrationstests trotz guter Unit-Tests nötig sind.
- Unterschied zwischen technischem Erfolg und fachlicher Akzeptanz beschreiben.

## Merksätze
- Je weiter oben in der Pyramide, desto realistischer und teurer.
- Viele kleine Tests unten entlasten die wenigen großen Tests oben.
- Schnittstellen sind klassische Fehlerquellen und deshalb Kern von Integrationstests.
