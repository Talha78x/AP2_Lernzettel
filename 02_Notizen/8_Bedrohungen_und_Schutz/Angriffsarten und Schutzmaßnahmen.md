# Angriffsarten und Schutzmanahmen

In FISI-Prüfungen müssen oft Schadensszenarien bewertet und Gegenmaßnahmen empfohlen werden. Das Thema hängt eng mit der [[Schutzbedafsanalyse und Riskoanalyse]] und den [[TOM|technischen und organisatorischen Maßnahmen]] zusammen.

**Wichtige Angriffsarten:**
- **Phishing / Social Engineering:** Angreifer manipulieren den "Faktor Mensch" (oft per E-Mail), um an Passwörter zu gelangen oder ihn dazu zu bringen, Malware auszuführen.
  *Schutz:* [[Grundlagen der IT-Sicherheit im beruflichen Alltag|Security Awareness Schulungen]], [[MFA, SSO, Passwortrichlinien|MFA]].
- **Ransomware:** Schadsoftware, die lokale Daten oder Netzwerkfreigaben verschlüsselt und Lösegeld fordert.
  *Schutz:* Isolierte/Offline-[[Backupstrategien Vollbackup, inkrementell, differentiell, kontinuierlich|Backups]], Netzwerksegmentierung (VLANs), Least-Privilege-Rechtevergabe.
- **DDoS (Distributed Denial of Service):** Tausende gekaperte Rechner (Botnet) überschütten einen Server mit Anfragen, bis dieser zusammenbricht (Verlust der [[Schutzziele der IT|Verfügbarkeit]]).
  *Schutz:* Load Balancer, Traffic-Scrubbing durch den Provider, Geoblocking.
- **SQL-Injection:** Angreifer schleusen über ungesicherte Eingabefelder auf einer Webseite (z. B. in einer [[Bildschirmausgabemasken|Suchmaske]]) böswilligen SQL-Code (z.B. `DROP TABLE`) in die [[Relationale, nicht relationale NoSQL Datenbanken|Datenbank]] ein.
  *Schutz:* Prepared Statements (Parametrisierte Abfragen), Input-Validierung, Web Application Firewalls (WAF).
- **Man-in-the-Middle (MitM) / Spoofing:** Der Angreifer klinkt sich unsichtbar zwischen Client und Server ein, liest Daten mit oder verfälscht sie (z. B. durch ARP-Spoofing im LAN).
  *Schutz:* Zwingende [[Verschlusselung Arten, Symmetrisch, Asymmetrisch, Hybride|Verschlüsselung (TLS/IPSec)]], Port-Security am Switch.
- **Brute-Force:** Der Angreifer probiert automatisiert tausende Passwortkombinationen aus, bis das richtige gefunden ist.
  *Schutz:* Kontosperrung nach x Fehlversuchen (Lockout-Policy), MFA, komplexe Passwörter.

Querverweise: [[Schutzziele der IT]], [[Zutritts-, Zugangs- und Zugriffskontrolle]], [[Firewall IDS, IPS, DMZ, ACL, Filtertabelle]].
