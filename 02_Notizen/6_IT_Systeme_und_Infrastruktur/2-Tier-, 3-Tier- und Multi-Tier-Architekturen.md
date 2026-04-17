# 2-Tier-, 3-Tier- und Multi-Tier-Architekturen

Bei der Architektur von IT-Anwendungen geht es darum, wie die logischen Aufgaben (Präsentation, Geschäftslogik, Datenhaltung) auf physische Systeme oder Server verteilt werden. 

**2-Tier-Architektur (Zweischicht-Modell):**
Eine klassische [[Client-Server und Peer-to-Peer|Client-Server-Umgebung]].
- *Tier 1 (Client):* Übernimmt die Präsentation (Benutzeroberfläche) und oft auch die Geschäftslogik ("Fat Client").
- *Tier 2 (Server):* Beinhaltet die Datenbank (z. B. einen SQL-Server).
- *Nachteil:* Wenn sich die Logik ändert, muss auf jedem Client ein Update eingespielt werden.

**3-Tier-Architektur (Dreischicht-Modell):**
Dies ist der heutige Standard für verteilte Systeme und Web-Anwendungen.
1. **Präsentationsschicht (Presentation Tier):** Die Benutzeroberfläche (oft ein Webbrowser oder "Thin Client").
2. **Logikschicht (Application Tier):** Hier läuft die eigentliche Datenverarbeitung und Geschäftslogik auf einem Applikations- oder Webserver.
3. **Datenschicht (Data Tier):** Ein dedizierter Datenbankserver (siehe [[Relationale, nicht relationale NoSQL Datenbanken]]), der nur die Daten speichert und auf Anfragen der Logikschicht antwortet.

*Vorteile der 3-Tier-Architektur:* Hohe Sicherheit (die Datenbank ist vom Nutzer getrennt), exzellente Skalierbarkeit (man kann mehr App-Server hinzufügen, ohne die Datenbank anzufassen) und leichtere Wartung.

Querverweise: [[Server und Storage]], [[On-Premises, Cloud, Housing, Hosting sowie IaaS, PaaS und SaaS]].
