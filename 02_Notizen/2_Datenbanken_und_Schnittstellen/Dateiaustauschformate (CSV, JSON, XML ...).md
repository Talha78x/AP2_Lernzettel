# Dateiaustauschformate CSV, JSON, XML ....

Beim Datenaustausch zwischen Systemen (z.B. über eine [[APIs und REST|REST-API]] oder bei Exporten aus Datenbanken) haben sich bestimmte maschinenlesbare Formate etabliert. Für Prüfungen müssen FISIs diese Formate lesen und unterscheiden können.

**1. CSV (Comma-Separated Values):**
Ein sehr simples, rein textbasiertes Format für Tabellendaten. Jede Zeile der Datei ist ein Datensatz, die einzelnen Spaltenwerte werden durch ein Trennzeichen (oft Komma oder Semikolon) getrennt.
*Vorteile:* Extrem platzsparend, leicht in Excel oder per Bash-Skript verarbeitbar.
*Nachteile:* Kann keine komplexen Verschachtelungen (Hierarchien) abbilden.

**2. XML (eXtensible Markup Language):**
Eine Auszeichnungssprache, die mit sogenannten Tags (`<Name>...</Name>`) arbeitet, ähnlich wie HTML. 
*Vorteile:* Kann sehr komplexe, verschachtelte Datenstrukturen abbilden.
*Nachteile:* Sehr gesprächig (Overhead durch viele Tags), dadurch große Dateigrößen und schwerer von Menschen zu lesen.

**3. JSON (JavaScript Object Notation):**
Das heute dominierende Format im Webumfeld und für NoSQL-Datenbanken. Daten werden in Schlüssel-Wert-Paaren (`"Name": "Mustermann"`) gespeichert und in geschweiften Klammern `{}` strukturiert. Listen werden in eckigen Klammern `[]` dargestellt.
*Vorteile:* Leichtgewichtig, für Menschen gut lesbar, kann komplexe Hierarchien abbilden, nativer Standard in der Webentwicklung.

Querverweise: [[APIs und REST]], [[Relationale, nicht relationale NoSQL Datenbanken]].
