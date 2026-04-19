# SLA

## Definition
Ein **Service Level Agreement (SLA)** ist eine vertragliche Vereinbarung über messbare Service-Qualität, z. B. Verfügbarkeit, Reaktionszeit, Wiederherstellungszeit und Supportfenster.

## Warum ist das so?
Kunden und IT brauchen klare Erwartungen. Ohne SLA gibt es Streit über „zu langsam“ oder „ausreichend schnell“.

## Zusammenspiel
- Monitoring liefert Messwerte ([[Monitoring und SNMP]]).
- Ticketsystem erfasst Reaktions- und Lösungszeiten ([[Ticketsysteme]]).
- Eskalationsstufen werden über Support-Level abgewickelt ([[1st-Level, 2nd-Level, 3rd-Level-Support]]).

## Typische SLA-Kennzahlen
| Kennzahl | Bedeutung | Beispiel |
|---|---|---|
| Verfügbarkeit | Anteil verfügbarer Zeit | 99,9 %/Monat |
| Reaktionszeit | Zeit bis Ticketbearbeitung startet | 30 Minuten |
| Wiederherstellungszeit (MTTR) | Zeit bis Service wieder nutzbar | 4 Stunden |
| Servicezeit | Zeitfenster der Leistungserbringung | Mo–Fr 8–18 Uhr |

## Rechenweg (prüfungsrelevant)
**Aufgabe:** Monat mit 30 Tagen, SLA 99,5 %. Wie viel Ausfallzeit ist maximal erlaubt?

Gesamtzeit = 30 × 24 × 60 = **43.200 Minuten**  
Erlaubter Ausfall = 0,5 % von 43.200 = **216 Minuten** (= 3 h 36 min)

## Eigene Worte
SLA ist die „Messlatte“ der IT-Leistung. Das SLA definiert **was** erreicht werden soll; SOP und Betrieb definieren **wie**.

## Typische Prüfungsszenarien
- Verfügbarkeitsrechnung in Minuten
- Unterschied OLA/UC/SLA
- Prioritätsmatrix nach Business-Impact

## Querverweise
[[Monitoring und SNMP]] · [[Ticketsysteme]] · [[SOP]] · [[Projektcontrolling]]
