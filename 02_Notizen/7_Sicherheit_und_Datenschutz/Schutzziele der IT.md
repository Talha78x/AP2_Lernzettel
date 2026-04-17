# Schutzziele der IT

Die Informationssicherheit basiert auf drei grundlegenden Schutzzielen, die oft als **CIA-Triade** (Confidentiality, Integrity, Availability) oder im Deutschen als **V-I-V** bezeichnet werden. In der IHK-Prüfung müssen FISIs fast immer Angriffe oder Schutzmaßnahmen diesen drei Zielen zuordnen.

1. **Vertraulichkeit (Confidentiality):**
   Daten dürfen nur von autorisierten Personen gelesen oder genutzt werden. Sie müssen vor unbefugtem Zugriff geschützt sein.
   *Typische Maßnahmen:* [[Verschlusselung Arten, Symmetrisch, Asymmetrisch, Hybride|Verschlüsselung (z.B. AES, TLS)]], Passwörter, [[Zutritts-, Zugangs- und Zugriffskontrolle]].
   *Typischer Angriff:* Sniffing, Man-in-the-Middle-Angriff.

2. **Integrität (Integrity):**
   Daten und Systeme müssen korrekt, vollständig und unverändert bleiben. Änderungen dürfen nur durch berechtigte Personen und nachvollziehbar erfolgen.
   *Typische Maßnahmen:* [[Hashverfahren digitale Signaturen|Prüfsummen (Hashes wie SHA-256)]], digitale Signaturen, restriktive Dateiberechtigungen.
   *Typischer Angriff:* Man-in-the-Middle (Verändern von Daten auf dem Transportweg), SQL-Injection.

3. **Verfügbarkeit (Availability):**
   IT-Systeme, Netzwerke und Daten müssen für berechtigte Nutzer zum geforderten Zeitpunkt nutzbar (verfügbar) sein.
   *Typische Maßnahmen:* [[Snap-Shot, Versionierung, Hochverfugbarkeit Clustering, Load Balancing, FHRP|Redundante Systeme (Clustering, Load Balancing)]], [[USV Arten, Vor- und Nachteile|USV-Anlagen]], [[Backupstrategien Vollbackup, inkrementell, differentiell, kontinuierlich|Backups]].
   *Typischer Angriff:* DDoS-Attacken, Ransomware (verschlüsselt Daten und macht sie unverfügbar).

Zusätzlich werden vom BSI oft noch erweiterte Schutzziele wie **Authentizität** (Ist der Absender wirklich der, der er vorgibt zu sein?) und **Verbindlichkeit / Nicht-Abstreitbarkeit** (Non-Repudiation) genannt.

Querverweise: [[Angriffsarten und Schutzmanahmen]], [[Schutzbedafsanalyse und Riskoanalyse]].
