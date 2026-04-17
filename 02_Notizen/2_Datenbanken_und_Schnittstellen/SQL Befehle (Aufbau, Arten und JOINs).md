# SQL Befehle Aufbau, Arten und JOINs

**SQL (Structured Query Language)** ist die Standardsprache zur Kommunikation mit [[Relationale, nicht relationale NoSQL Datenbanken|relationalen Datenbanken]]. In Prüfungen wird oft verlangt, SELECT-Abfragen zu schreiben oder Fehler darin zu finden.

Die Befehle werden grob in Kategorien eingeteilt:
- **DML (Data Manipulation Language):** Daten bearbeiten (`SELECT`, `INSERT`, `UPDATE`, `DELETE`).
- **DDL (Data Definition Language):** Tabellenstruktur ändern (`CREATE TABLE`, `DROP`, `ALTER`).

**Grundaufbau eines DML-Befehls:**
``sql
SELECT Spalte1, Spalte2     -- Welche Daten sollen ausgegeben werden?
FROM Tabelle                -- Aus welcher Tabelle?
WHERE Bedingung             -- Filterkriterien (z.B. Alter > 18)
ORDER BY Spalte1 ASC;       -- Sortierung (aufsteigend oder DESC für absteigend)


#### JOINs: 
Um Daten aus mehreren, über Schlüssel verbundenen Tabellen (siehe [ER-Modell Attribute, Beziehungen, Kardinalitaten, referenzielle Integritat]) abzufragen, nutzt man JOINs.
•	INNER JOIN: Gibt nur die Datensätze zurück, bei denen es in beiden Tabellen eine Übereinstimmung (meist Primär- zu Fremdschlüssel) gibt.
•	LEFT (OUTER) JOIN: Gibt alle Datensätze aus der linken (zuerst genannten) Tabelle zurück und nur die passenden aus der rechten. Findet sich rechts nichts, werden die Felder mit  NULL  aufgefüllt.
•	RIGHT (OUTER) JOIN: Das Gegenteil vom Left Join (gibt alle Daten der rechten Tabelle zurück).
•	CROSS JOIN: Jeder Datensatz der ersten Tabelle wird mit jedem der zweiten kombiniert (kartesisches Produkt). In der Praxis meist unerwünscht, wenn es unabsichtlich durch ein vergessenes  WHERE  oder  ON  passiert.
	
	
	