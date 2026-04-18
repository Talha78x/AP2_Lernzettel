# Dateifreigaben und Datenabruf, z. B. SMB, CIFS und ODBC

## Definition
Für den Zugriff auf zentrale Ressourcen im Netzwerk gibt es unterschiedliche Verfahren:

- **SMB (Server Message Block):** Protokoll für Datei- und Druckerfreigaben, vor allem in Windows-Umgebungen
- **CIFS:** ältere, unsichere SMB-Variante bzw. historische Bezeichnung im Umfeld von SMB 1
- **ODBC (Open Database Connectivity):** standardisierte Schnittstelle für den Zugriff auf Datenbanken

Wichtig ist: SMB/CIFS und ODBC lösen **nicht** dasselbe Problem.

## Warum ist das so?
Im Netzwerk will man zentrale Ressourcen auf zwei sehr unterschiedliche Arten nutzen:
- als **Datei**, zum Beispiel ein gemeinsamer Ordner
- als **strukturierte Datenquelle**, zum Beispiel eine SQL-Datenbank

Deshalb braucht man unterschiedliche Protokolle und Schnittstellen. Ein Dateifreigabeprotokoll stellt Dateien bereit, eine Datenbankschnittstelle liefert Datensätze und Abfragen.

## Zusammenspiel
- [[Client-Server und Peer-to-Peer]] erklärt das zugrunde liegende Kommunikationsmodell.
- [[Netzwerkkomponenten]] zeigt, über welche Infrastruktur solche Dienste erreichbar werden.
- [[Relationale, nicht relationale & NoSQL Datenbanken]] und [[SQL Befehle (Aufbau, Arten und JOINs)]] sind bei ODBC fachlich eng verknüpft.
- [[Active Directory und LDAP]] spielt bei SMB-Freigaben oft bei Anmeldung und Rechtevergabe mit hinein.
- [[Standardprotokolle (TCP, UDP, MAC, ARP, ICMP, HTTP, HTTPS, FTP, SMTP...)]] liefert den Protokollkontext.

## Eigene Worte (prüfungsnah)
SMB stellt mir typischerweise einen Ordner oder Drucker im Netzwerk bereit. ODBC gibt mir dagegen keine Dateien, sondern einen standardisierten Weg, aus Anwendungen heraus auf Datenbanken zuzugreifen.

## SMB und CIFS
| Begriff | Bedeutung | Prüfungsrelevanter Punkt |
|---|---|---|
| SMB | modernes Datei- und Druckerfreigabeprotokoll | Standard in Windows-Netzen |
| CIFS | alte SMB-Variante / SMBv1-Umfeld | heute veraltet und unsicher |
| Samba | Linux/Unix-Implementierung für SMB-Dienste | wichtig für gemischte Umgebungen |

### Typische SMB-Einsätze
- Netzlaufwerke
- gemeinsame Teamordner
- zentrale Druckerfreigaben
- Datei-Server in Windows-Domänen

**Wichtig:** SMBv1/CIFS sollte heute vermieden oder deaktiviert werden.

## ODBC
ODBC ist keine Dateifreigabe, sondern eine **Datenbankschnittstelle**.

| Merkmal | ODBC |
|---|---|
| Zweck | standardisierter Zugriff auf Datenbanken |
| Ebene | Anwendung greift auf DBMS zu |
| Vorteil | gleiche Schnittstellenlogik trotz unterschiedlicher Datenbanken |
| Beispiel | Reporting-Tool liest Daten aus MSSQL oder MySQL |

## SMB vs. ODBC
| Frage | SMB / CIFS | ODBC |
|---|---|---|
| Gibt Dateien frei? | ja | nein |
| Greift auf Datenbankinhalte zu? | nicht direkt | ja |
| Typischer Client | Dateiexplorer, Office, Betriebssystem | Fachanwendung, Reporting-Tool |
| Typischer Server | Fileserver | Datenbankserver |

## Typische Ports und Praxis
| Technik | Typischer Punkt |
|---|---|
| SMB | häufig TCP 445 |
| CIFS / Altumgebungen | historisch auch 139 / NetBIOS-Kontext |
| ODBC | nutzt je nach Datenbanksystem unterschiedliche DB-Ports |

## Beispielaufgabe mit Lösung
**Aufgabe:** Eine Benutzerin soll in einem Netz auf einen gemeinsamen Projektordner zugreifen. Ein Controlling-Tool soll dagegen Verkaufsdaten direkt aus einer SQL-Datenbank abrufen. Welche Technik passt jeweils?

**Lösung:**
- gemeinsamer Projektordner -> **SMB**
- Abruf strukturierter Daten aus der Datenbank -> **ODBC**

**Begründung:**
SMB ist für Dateiressourcen gedacht, ODBC für Datenbankzugriffe aus Anwendungen.

## Typische Prüfungsszenarien
- SMB und ODBC sauber unterscheiden.
- erklären, warum CIFS/SMBv1 problematisch ist.
- Datei- und Druckerfreigabe von Datenbankzugriff abgrenzen.
- Samba in gemischten Netzen einordnen.

## Merksätze
- SMB teilt Dateien, ODBC verbindet Anwendungen mit Datenbanken.
- CIFS ist historisch und sicherheitstechnisch problematisch.
- Nicht jede Netzwerkfreigabe ist eine Datenbankschnittstelle.
