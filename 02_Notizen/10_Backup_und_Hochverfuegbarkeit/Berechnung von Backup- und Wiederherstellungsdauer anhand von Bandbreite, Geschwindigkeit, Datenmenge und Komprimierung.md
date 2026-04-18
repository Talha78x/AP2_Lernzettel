# Berechnung von Backup- und Wiederherstellungsdauer anhand von Bandbreite, Geschwindigkeit, Datenmenge und Komprimierung

## Definition
Bei diesen Aufgaben wird berechnet, wie lange Backups oder Restores dauern und wie viel Speicherplatz benötigt wird. Typische Größen sind:
- Datenmenge
- Übertragungsrate
- Protokoll-Overhead
- Komprimierung

## Warum ist das so?
Backup-Konzepte müssen praktisch umsetzbar sein. Es reicht nicht zu sagen "wir sichern jede Nacht", wenn:
- das Backupfenster zu klein ist
- die Internetleitung zu langsam ist
- der Restore Tage dauern würde

Darum sind Zeit- und Größenberechnungen ein klassisches Prüfungsthema.

## Zusammenspiel
- [[Backupstrategien (Vollbackup, inkrementell, differentiell, kontinuierlich)]] liefert den Sicherungstyp.
- [[Notfallkonzept, Disaster Recovery]] nutzt die Ergebnisse für RTO und RPO.
- [[Anforderungen an Bandbreite, Latenz, Verfügbarkeit, Übertragungsmedien und Netzwerksicherheit]] ergänzt die Netzperspektive.
- [[Band, Platte, NAS, SAN, Cloud, USB und optische Datenträger als Sicherungsmedien]] beeinflusst reale Geschwindigkeit und Kapazität.

## Eigene Worte (prüfungsnah)
Diese Aufgaben prüfen, ob man Datenmengen, Bandbreiten und Speicherbedarf sauber umrechnen kann. Der häufigste Fehler ist dabei die Verwechslung von **Bit und Byte**.

## Grundformeln
| Gesucht | Formel |
|---|---|
| Zeit | `Zeit = Datenmenge / Übertragungsrate` |
| Speicher nach Komprimierung | `Datenmenge x Restfaktor` |
| Nutzrate bei Overhead | `theoretische Rate x Nutzanteil` |

## Bit und Byte
| Größe | Umrechnung |
|---|---|
| 1 Byte | 8 Bit |
| 1 Gbit/s | 125 MByte/s theoretisch |
| 1 TB | je nach Aufgabe 1000 GB oder 1024 GB beachten |

**Wichtig:** In Prüfungen immer genau lesen, ob dezimal oder binär gerechnet werden soll.

## Typischer Rechenweg
1. Datenmenge in passende Einheit umrechnen.
2. Bandbreite in **Byte pro Sekunde** umrechnen, falls nötig.
3. Overhead berücksichtigen.
4. Komprimierung berücksichtigen.
5. Ergebnis in Minuten oder Stunden umwandeln.

## Beispielaufgabe mit Lösung
**Aufgabe:** 2 TB Daten sollen über eine 1-Gbit/s-Leitung gesichert werden. Wegen Overhead sind nur 80 % der Bandbreite nutzbar. Wie lange dauert das Backup ungefähr?

**Lösung:**
1. 1 Gbit/s = 125 MByte/s theoretisch
2. 80 % davon = `125 x 0,8 = 100 MByte/s`
3. 2 TB = `2.000.000 MByte` bei Dezimalannahme
4. Zeit = `2.000.000 / 100 = 20.000 s`
5. `20.000 s / 3600 ≈ 5,56 h`

**Ergebnis:**
Das Backup dauert ungefähr **5,6 Stunden**.

## Komprimierung
| Angabe | Bedeutung |
|---|---|
| 2:1 | Datenmenge halbiert sich |
| 30 % Einsparung | Restmenge = 70 % |

**Beispiel:**
5 TB mit 30 % Einsparung -> `5 TB x 0,7 = 3,5 TB`

## Typische Prüfungsfallen
- Bit mit Byte verwechseln
- Overhead vergessen
- 1000 und 1024 vermischen
- Restorezeit und Backupzeit gleichsetzen, obwohl Praxis anders sein kann

## Typische Prüfungsszenarien
- Dauer eines Vollbackups berechnen.
- Speicherbedarf verschiedener Strategien vergleichen.
- Komprimierung einrechnen.
- effektive statt theoretische Bandbreite nutzen.

## Merksätze
- Erst Einheiten sauber machen, dann rechnen.
- Gbit/s ist nicht GByte/s.
- In Prüfungen kostet nicht die Formel Punkte, sondern meist die falsche Umrechnung.
