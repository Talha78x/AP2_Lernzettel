# Relationale, nicht relationale NoSQL Datenbanken

In der modernen IT gibt es zwei große Kategorien von Datenbanksystemen, die unterschiedliche Einsatzzwecke haben.

**Relationale Datenbanken (SQL):**
Daten werden in fest strukturierten Tabellen (Relationen) aus Zeilen und Spalten gespeichert. Tabellen sind über Primär- und Fremdschlüssel miteinander verknüpft (siehe [[ER-Modell Attribute, Beziehungen, Kardinalitaten, referenzielle Integritat]]).
- *Eigenschaften:* Festes Schema, starke Datenkonsistenz (ACID-Prinzip), gut für komplexe Abfragen mittels [[SQL Befehle Aufbau, Arten und JOINs]].
- *Einsatzgebiet:* ERP-Systeme, Finanzdaten, Warenwirtschaft. (Beispiele: MySQL, PostgreSQL, Oracle).

**Nicht-relationale Datenbanken (NoSQL):**
NoSQL steht für "Not only SQL". Hier werden Daten nicht in starren Tabellen, sondern flexibel gespeichert. Das Schema kann sich während des Betriebs ändern.
- *Kategorien:* Dokumentenorientiert (JSON-Dokumente), Key-Value-Stores (Schlüssel-Wert-Paare), Graphdatenbanken, Spaltenorientiert.
- *Eigenschaften:* Extrem gut horizontal skalierbar (über viele Server verteilbar), hohe Performance bei riesigen, unstrukturierten Datenmengen (Big Data), Verzicht auf strikte Konsistenz zugunsten von Verfügbarkeit.
- *Einsatzgebiet:* Web-Apps mit riesigem Traffic, [[Cyber-physische Systeme Sensoren, Aktoren und Bibliotheken|IoT-Sensordaten]], Social Media Feeds. (Beispiele: MongoDB, Redis, Cassandra).
