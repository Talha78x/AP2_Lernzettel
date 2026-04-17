# Hashverfahren digitale Signaturen

Hashverfahren und digitale Signaturen sichern die Schutzziele der [[Schutzziele der IT|Integrität und Authentizität]]. Sie stellen sicher, dass Daten auf dem Weg nicht verändert wurden und der Absender wirklich der ist, für den er sich ausgibt.

**Hashverfahren:**
Eine Hash-Funktion berechnet aus einer Eingabe beliebiger Länge (z.B. einer 5 GB großen Datei oder einem Passwort) eine Zeichenkette mit fester Länge (den Hashwert oder "Fingerabdruck").
- *Eigenschaften:* Sie funktioniert nur in eine Richtung (Einwegfunktion, man kann aus dem Hash nicht die Datei zurückberechnen). Kleinste Änderungen an der Datei verändern den Hashwert komplett (Lawineneffekt).
- *Verwendung:* Speicherung von Passwörtern (niemals im Klartext!), Überprüfung von Downloads (Prüfsummen).
- *Bekannte Algorithmen:* SHA-256, SHA-3 (MD5 und SHA-1 gelten als veraltet und unsicher).

**Digitale Signatur:**
Eine digitale Signatur beweist den Absender und die Unverfälschtheit eines Dokuments. Sie nutzt [[Verschlusselung Arten, Symmetrisch, Asymmetrisch, Hybride|asymmetrische Verschlüsselung]], aber "rückwärts":
1. Der Sender erstellt einen Hashwert seines Dokuments.
2. Der Sender verschlüsselt diesen Hashwert mit seinem **eigenen Private Key**. Das ist die Signatur.
3. Der Empfänger entschlüsselt die Signatur mit dem **Public Key des Senders** (beweist: Der Sender war es wirklich).
4. Der Empfänger bildet selbst den Hash vom Dokument und vergleicht ihn mit dem entschlüsselten Hash (beweist: Das Dokument wurde nicht manipuliert).

Querverweise: [[Zertifikate]], [[Schutzziele der IT]].
