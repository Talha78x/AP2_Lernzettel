# Troubleshooting und Härtungsmaßnahmen

## Definition
**Troubleshooting** ist strukturierte Fehleranalyse. **Härtung** reduziert die Angriffsfläche eines Systems.

## Warum ist das so?
Ungeplante Ausfälle sind teuer; Sicherheitslücken werden aktiv ausgenutzt. Beides wird durch Standards und Methodik beherrschbar.

## Zusammenspiel (Ablauf)
1. Störung erkennen ([[Monitoring und SNMP]])
2. Betroffene Systeme eingrenzen
3. Hypothesen prüfen (Logs, Pakete, Konfiguration)
4. Workaround + Root-Cause beheben
5. Härtungsmaßnahmen ergänzen, damit der Fehler nicht wiederkehrt

## Härtungs-Checkliste
| Bereich | Maßnahme |
|---|---|
| Accounts | MFA, least privilege, starke Policies |
| Dienste | Unnötige Services deaktivieren |
| Netzwerk | Segmentierung, ACL, sichere Protokolle |
| OS | Patchen, sichere Baselines, Logging |
| Anwendung | Eingabevalidierung, Secrets-Management |

## Eigene Worte
Troubleshooting beantwortet: "Warum ist es kaputt?" – Härtung beantwortet: "Wie verhindern wir den nächsten Vorfall?"

## Beispielaufgabe
**Aufgabe:** Webdienst nicht erreichbar, Ping funktioniert. Nenne den nächsten sinnvollen Prüfschritt.  
**Lösung:** Dienst- und Portprüfung (z. B. `ss -tulpen`, Reverse Proxy, Firewall-Regel). Netz ist erreichbar, also liegt der Fehler eher auf Transport-/Anwendungsebene.

## Prüfungsszenarien
- OSI-basiertes Troubleshooting darstellen
- Hardening von Linux/Windows beispielhaft nennen
- Root Cause vs. Symptom trennen

## Querverweise
[[SOP]] · [[SIEM usw...]] · [[Standardprotokolle (TCP, UDP, MAC, ARP, ICMP, HTTP, HTTPS, FTP, SMTP...)]]
