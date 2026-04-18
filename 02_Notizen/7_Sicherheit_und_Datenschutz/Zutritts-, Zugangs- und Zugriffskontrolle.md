# Zutritts-, Zugangs- und Zugriffskontrolle

## Definition
Diese drei Kontrollen beschreiben unterschiedliche Schutzebenen:
- **Zutrittskontrolle**: Wer darf physisch an einen Ort?
- **Zugangskontrolle**: Wer darf ein System benutzen?
- **Zugriffskontrolle**: Wer darf innerhalb des Systems auf welche Daten oder Funktionen zugreifen?

## Warum ist das so?
Sicherheit muss entlang des gesamten Wegs zur Information wirken:
1. Unbefugte sollen nicht einfach in sensible Räume gelangen.
2. Sie sollen sich nicht an Systemen anmelden können.
3. Selbst angemeldete Benutzer sollen nicht alles sehen oder ändern dürfen.

Ohne diese Trennung würden wichtige Schutzstufen vermischt.

## Zusammenspiel
- [[TOM]] nutzt diese Kontrollen als klassische Maßnahmen.
- [[Berechtigungskonzepte]] vertieft besonders die Zugriffskontrolle.
- [[MFA, SSO, Passwortrichtlinien]] gehört stark zur Zugangskontrolle.
- [[DSGVO und IT-Grundschutz (Personbezogene Daten usw..)]] fordert für personenbezogene Daten passende Schutzmaßnahmen.

## Eigene Worte (prüfungsnah)
Die drei Begriffe beschreiben denselben Schutzweg auf unterschiedlichen Ebenen: erst in den Raum, dann an das System, dann an die Daten. Genau diese Reihenfolge hilft auch in Prüfungen beim Unterscheiden.

## Die drei Ebenen
| Ebene | Frage | Beispiele |
|---|---|---|
| Zutritt | Wer darf physisch hinein? | Schließsystem, Chipkarte, Wachdienst |
| Zugang | Wer darf sich am System anmelden? | Passwort, MFA, Smartcard, VPN-Login |
| Zugriff | Was darf ein angemeldeter Nutzer tun? | NTFS-Rechte, Rollen, Freigabeberechtigungen |

## Typische Prüfungsfalle
Ein Passwort am Windows-Login ist **keine Zutrittskontrolle**, sondern **Zugangskontrolle**.

Ein Schlüsselschloss am Serverraum ist **keine Zugriffskontrolle**, sondern **Zutrittskontrolle**.

## Beispiele im Zusammenspiel
| Situation | richtige Einordnung |
|---|---|
| Fingerprint am Serverraum | Zutrittskontrolle |
| Anmeldung mit Benutzername, Passwort und Token | Zugangskontrolle |
| Benutzer darf nur seinen Abteilungsordner öffnen | Zugriffskontrolle |

## Beispielaufgabe mit Lösung
**Aufgabe:** Ein Mitarbeiter darf das Firmengebäude betreten und sich am PC anmelden, kann aber die Personalakten nicht öffnen. Welche Kontrolle wirkt an dieser Stelle?

**Lösung:**
**Zugriffskontrolle**

**Begründung:**
Zutritt und Zugang sind bereits erfolgt. Jetzt geht es darum, welche Daten innerhalb des Systems gelesen oder bearbeitet werden dürfen.

## Typische Prüfungsszenarien
- Zutritt, Zugang und Zugriff sauber voneinander trennen.
- Beispiele richtig zuordnen.
- erklären, warum ein erfolgreicher Login noch nicht alle Rechte bedeutet.
- diese Kontrollen als TOMs einordnen.

## Merksätze
- Zutritt = Raum.
- Zugang = System.
- Zugriff = Daten/Funktion.
- Die Reihenfolge ist die beste Eselsbrücke für Prüfungsfragen.
