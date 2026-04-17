# ER-Modell Attribute, Beziehungen, Kardinalitaten, referenzielle Integritat

Das **Entity-Relationship-Modell (ER-Modell oder ERM)** ist der erste Schritt beim Datenbankdesign. Es ist eine grafische Darstellung, um Objekte und deren Beziehungen zueinander logisch zu planen, bevor man Tabellen mit [[SQL Befehle Aufbau, Arten und JOINs|SQL]] anlegt.

**Grundbegriffe:**
- **Entität (Entity):** Ein reales oder abstraktes Objekt, das beschrieben werden soll (z.B. Kunde, Artikel). Im Modell ein Rechteck. Daraus wird später eine Tabelle.
- **Attribut:** Eine Eigenschaft der Entität (z.B. Vorname, Preis). Im Modell eine Ellipse. Ein Attribut, das einen Datensatz eindeutig identifiziert, wird zum **Primärschlüssel**.
- **Beziehung (Relationship):** Die Verknüpfung zwischen Entitäten (z.B. "Kunde *bestellt* Artikel"). Im Modell eine Raute.

**Kardinalitäten:**
Sie geben an, in welchem Zahlenverhältnis die Entitäten zueinander stehen (z.B. nach der Chen-Notation):
- **1:1** – Eine Entität steht mit genau einer anderen in Beziehung (z.B. Mitarbeiter - Firmenwagen).
- **1:n** – Eine Entität steht mit vielen in Beziehung, die andere aber nur mit einer (z.B. Abteilung - Mitarbeiter).
- **n:m** – Viele stehen mit vielen in Beziehung (z.B. Schüler - Kurse). Eine n:m-Beziehung muss bei der Umsetzung in die Datenbank immer in eine Zwischentabelle aufgelöst werden.

**Referenzielle Integrität:**
Dieses Prinzip stellt sicher, dass Beziehungen zwischen Tabellen gültig bleiben. Ein **Fremdschlüssel** in einer Tabelle darf nur Werte enthalten, die als Primärschlüssel in der verknüpften Tabelle tatsächlich existieren. Es verhindert zum Beispiel, dass man einen Kunden aus der Datenbank löscht, der noch aktive Rechnungen hat (sogenannte "Dateileichen").

Querverweise: [[Normalisierung Regeln]], [[UML Diagramme]].
