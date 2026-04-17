# Normalisierung Regeln

**Normalisierung** ist der Prozess, bei dem das [[ER-Modell Attribute, Beziehungen, Kardinalitaten, referenzielle Integritat|Datenmodell]] einer relationalen Datenbank strukturiert wird, um **Redundanzen** (doppelte Daten) zu vermeiden und **Anomalien** (Fehler beim Ändern, Löschen oder Einfügen) zu verhindern. In IHK-Prüfungen müssen oft Tabellen bis zur 3. Normalform (3NF) überführt werden.

**Die drei wichtigsten Normalformen:**

**1. Normalform (1NF):**
Eine Tabelle ist in der 1NF, wenn alle Attributwerte **atomar** sind. Das bedeutet, ein Feld darf nicht weiter sinnvoll in mehrere Werte zerlegt werden können.
*Beispiel:* Das Feld `Adresse="Musterstr. 1, 12345 Stadt"` ist *nicht* atomar. Es muss aufgeteilt werden in `Straße`, `Hausnummer`, `PLZ` und `Ort`. Zudem dürfen keine Wiederholungsgruppen (z.B. Telefon1, Telefon2) vorkommen.

**2. Normalform (2NF):**
Eine Tabelle ist in der 2NF, wenn sie in der 1NF ist *und* jedes Nicht-Schlüsselattribut voll vom **gesamten** Primärschlüssel abhängt. 
*Wichtig:* Dies ist nur relevant, wenn die Tabelle einen **zusammengesetzten** Primärschlüssel (z.B. aus `Kunden_ID` und `Artikel_ID`) hat. Hängt der Kundenname nur von der `Kunden_ID` ab, verletzt das die 2NF und muss in eine eigene Kundentabelle ausgelagert werden.

**3. Normalform (3NF):**
Eine Tabelle ist in der 3NF, wenn sie in der 2NF ist *und* keine **transitiven Abhängigkeiten** existieren. Das bedeutet: Kein Nicht-Schlüsselattribut darf von einem anderen Nicht-Schlüsselattribut abhängen.
*Beispiel:* In einer Mitarbeitertabelle mit der `Abteilungs_ID` darf nicht auch noch der `Abteilungsname` stehen, da dieser von der `Abteilungs_ID` (einem Nicht-Schlüsselattribut für den Mitarbeiter) abhängt. Die Abteilung muss in eine eigene Tabelle.

Kurze Eselsbrücke: *"Die Daten hängen vom Schlüssel ab (1NF), vom ganzen Schlüssel (2NF) und von nichts als dem Schlüssel (3NF)."*
