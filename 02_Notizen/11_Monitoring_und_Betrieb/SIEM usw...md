# SIEM usw...

## Definition
**SIEM (Security Information and Event Management)** sammelt, korreliert und bewertet Sicherheitsereignisse aus vielen Quellen (Logs, Firewalls, AD, EDR, Cloud), um Angriffe schneller zu erkennen.

## Warum ist das so?
Einzelne Logs zeigen nur Ausschnitte. Ein Angriff wird oft erst sichtbar, wenn mehrere Ereignisse kombiniert werden (z. B. Login-Fehler + neuer Admin + Datenabfluss).

## Zusammenspiel im Betrieb
- Logquellen aus Infrastruktur, Anwendungen und Identity-Systemen
- Normalisierung der Daten in ein gemeinsames Schema
- Korrelation (Regeln/Use Cases), z. B. "5 Fehlanmeldungen + erfolgreicher Login aus neuem Land"
- Alarmierung und Übergabe in [[Ticketsysteme]] / SOC-Prozess
- Nachbearbeitung in [[SOP]] und [[Troubleshooting und Härtungsmaßnahmen]]

## SIEM, SOAR, XDR (Abgrenzung)
| Begriff | Fokus |
|---|---|
| SIEM | Sammeln + Korrelation + Alarmierung |
| SOAR | Automatisierte Reaktion (Playbooks) |
| XDR | Erweiterte Erkennung über Endpoint/Netzwerk/Cloud |

## Eigene Worte
SIEM ist die "Sicherheitszentrale" für Logdaten: Es reduziert Rauschen, priorisiert relevante Vorfälle und schafft Revisionssicherheit.

## Beispielaufgabe
**Aufgabe:** Warum ist ein SIEM ohne Zeit-Synchronisation problematisch?  
**Lösung:** Ohne einheitliche Zeitstempel können Ereignisse nicht korrekt korreliert werden. Ursache-Wirkung wird unklar.

## Prüfungsszenarien
- SIEM-Ziele nennen (Erkennung, Nachvollziehbarkeit, Compliance)
- False Positive vs. False Negative erklären
- Korrelation an einem Beispiel erläutern

## Querverweise
[[Monitoring und SNMP]] · [[SOP]] · [[SLA]] · [[Hashverfahren & digitale Signaturen]]
