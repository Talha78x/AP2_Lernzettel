# Verschlusselung Arten, Symmetrisch, Asymmetrisch, Hybride

Verschlüsselung (Kryptographie) sichert das Schutzziel der [[Schutzziele der IT|Vertraulichkeit]]. In der IHK-Prüfung muss man die drei grundlegenden Verfahren sicher unterscheiden können.

**1. Symmetrische Verschlüsselung:**
- Sender und Empfänger nutzen **denselben Schlüssel** zum Ver- und Entschlüsseln.
- *Vorteile:* Extrem schnell, gut für große Datenmengen (z.B. Festplattenverschlüsselung oder Payload-Daten im Netzwerk).
- *Nachteile:* Das Schlüsselaustausch-Problem (Wie kommt der Schlüssel sicher zum Empfänger, bevor verschlüsselt kommuniziert wird?).
- *Bekannte Algorithmen:* AES (Advanced Encryption Standard), DES.

**2. Asymmetrische Verschlüsselung:**
- Jeder Teilnehmer hat ein **Schlüsselpaar**: Einen **Public Key** (öffentlich, darf jeder kennen) und einen **Private Key** (streng geheim). Was mit dem Public Key verschlüsselt wird, kann *nur* mit dem Private Key wieder entschlüsselt werden.
- *Vorteile:* Löst das Problem des Schlüsselaustauschs. 
- *Nachteile:* Mathematisch sehr aufwendig und langsam, nicht für große Datenmengen geeignet.
- *Bekannte Algorithmen:* RSA, Elliptische Kurven (ECC).

**3. Hybride Verschlüsselung:**
- Kombiniert die Vorteile beider Verfahren. So funktioniert z.B. [[TLS SSL]] oder PGP:
  1. Der Sender generiert einen zufälligen symmetrischen Schlüssel (Session Key).
  2. Die eigentlichen Nutzdaten (groß) werden mit dem symmetrischen Schlüssel schnell verschlüsselt.
  3. Der symmetrische Session Key selbst (klein) wird asymmetrisch mit dem Public Key des Empfängers verschlüsselt und mitgeschickt.
  4. Der Empfänger entschlüsselt mit seinem Private Key zuerst den Session Key und damit dann die großen Nutzdaten.

Querverweise: [[Hashverfahren digitale Signaturen]], [[Zertifikate]].
