# Befehlezeilenkomandos (ping, tracert, nslookup, ipconfig, ifconfig, netstat, nmap, tcpdump, dig ...)

## Definition
Befehlszeilenkommandos sind Werkzeuge zur Analyse, Konfiguration und Fehlersuche in Netzwerken und Systemen. Sie helfen, Verbindungen, Adressen, Namensauflösung, Ports und Datenverkehr zu prüfen.

## Warum ist das so?
Bei Störungen reicht ein Blick in die Oberfläche oft nicht aus. Administratoren müssen systematisch prüfen:
- Hat das Gerät eine gültige IP?
- Ist das Ziel erreichbar?
- Funktioniert DNS?
- Wo bricht der Weg ab?
- Lauscht ein Dienst auf dem erwarteten Port?

CLI-Werkzeuge liefern dafür schnelle und gezielte Antworten.

## Zusammenspiel
- [[Standardprotokolle (TCP, UDP, MAC, ARP, ICMP, HTTP, HTTPS, FTP, SMTP...)]] erklärt die Protokollbasis vieler Kommandos.
- [[Netzwerkrelevante Dienste (DHCP, DNS, NTP, SNMP...)]] spielt besonders bei `nslookup`, `dig` und IP-Konfiguration mit hinein.
- [[OSI und TCP-IP Modell]] hilft bei der schichtweisen Einordnung der Ergebnisse.
- [[Troubleshooting und Härtungsmaßnahmen]] ist die betriebliche Ergänzung.

## Eigene Worte (prüfungsnah)
Die Kommandos sind Werkzeuge für eine systematische Fehlersuche. Statt zu raten, prüft man Schritt für Schritt: lokale Konfiguration, Erreichbarkeit, Namensauflösung, Weg durchs Netz und offene Dienste.

## Wichtige Kommandos
| Kommando | Zweck | Typischer Nutzen |
|---|---|---|
| `ping` | Erreichbarkeit prüfen | Host antwortet auf ICMP oder nicht |
| `tracert` / `traceroute` | Weg zum Ziel prüfen | zeigt Hops und mögliche Abbruchstelle |
| `ipconfig` / `ifconfig` / `ip` | lokale Konfiguration anzeigen | IP, Gateway, DNS prüfen |
| `nslookup` / `dig` | DNS-Abfragen stellen | Namensauflösung testen |
| `netstat` | Verbindungen und Ports anzeigen | prüfen, ob ein Dienst lauscht |
| `nmap` | Hosts und Ports scannen | Netz- und Dienstübersicht |
| `tcpdump` / Wireshark | Pakete mitschneiden | detaillierte Analyse des Verkehrs |

## Typische Einordnung
| Frage | Passendes Werkzeug |
|---|---|
| Habe ich eine gültige IP-Adresse? | `ipconfig`, `ifconfig`, `ip` |
| Ist das Ziel grundsätzlich erreichbar? | `ping` |
| Wo endet die Strecke? | `tracert` / `traceroute` |
| Funktioniert DNS? | `nslookup`, `dig` |
| Ist Port 443 offen? | `netstat`, `nmap` |
| Was wird wirklich übertragen? | `tcpdump`, Wireshark |

## Kurz erklärt
### `ping`
- nutzt meist ICMP Echo Request/Reply
- prüft Layer-3-Erreichbarkeit
- kein Beweis, dass ein Dienst wie HTTP funktioniert

### `tracert` / `traceroute`
- zeigt Router-Hops
- hilft beim Eingrenzen von Routingproblemen

### `nslookup` / `dig`
- prüft DNS direkt
- wichtig bei "IP geht, Name nicht"

### `netstat`
- zeigt offene Ports und Verbindungen
- hilfreich bei lokalen Dienstproblemen

### `tcpdump`
- zeigt echte Pakete
- sehr nützlich, wenn Ursache unklar bleibt

## Beispielaufgabe mit Lösung
**Aufgabe:** Ein Server ist per IP erreichbar, aber `intranet.firma.local` funktioniert nicht. Welches Kommando ist jetzt am sinnvollsten?

**Lösung:**
`nslookup` oder `dig`

**Begründung:**
Wenn die Verbindung per IP funktioniert, ist das Grundnetz vorhanden. Das Problem liegt wahrscheinlich in der Namensauflösung.

## Typische Prüfungsszenarien
- passendes Kommando für ein Fehlerszenario auswählen.
- `ping` von `traceroute` unterscheiden.
- erklären, warum `ping` allein keinen funktionierenden Webdienst beweist.
- DNS-Fehler von Routing- oder IP-Fehlern abgrenzen.

## Merksätze
- Erst lokale Konfiguration prüfen, dann das Ziel.
- IP erreichbar heißt nicht automatisch, dass DNS oder der Dienst funktioniert.
- Paketmitschnitt ist oft der tiefste Blick in das Problem.
