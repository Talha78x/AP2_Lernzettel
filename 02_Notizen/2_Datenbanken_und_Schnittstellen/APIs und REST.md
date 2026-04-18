# APIs und REST

## Definition
Eine API ist eine definierte Schnittstelle zwischen Systemen. REST ist ein Architekturstil für HTTP-basierte APIs.

## Warum ist das so?
Systeme sollen entkoppelt kommunizieren können: klarer Vertrag statt direktem Datenbankzugriff.

## Zusammenspiel
Client -> API -> Business-Logik -> Datenbank.
Bezug zu [[SQL Befehle (Aufbau, Arten und JOINs)]], [[Dateiaustauschformate (CSV, JSON, XML ...)]] und [[OpenData]].

## REST-Grundlagen
| HTTP-Methode | Zweck |
|---|---|
| GET | lesen |
| POST | anlegen |
| PUT/PATCH | ändern |
| DELETE | löschen |

## Beispielaufgabe
**Aufgabe:** `GET /users/42` liefert 404. Wie prüfen?

**Lösung:**
1. Existiert Ressource 42?
2. Route korrekt?
3. Authentifizierung/Autorisierung korrekt?
4. API-Log und DB-Abfrage prüfen.
