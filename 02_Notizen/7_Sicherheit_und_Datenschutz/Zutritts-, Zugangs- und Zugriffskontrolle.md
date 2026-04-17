# Zutritts-, Zugangs- und Zugriffskontrolle

Um IT-Systeme abzusichern (und um die Vorgaben der [[DSGVO und IT-Grundschutz Personbezogene Daten usw...|DSGVO]] zu erfüllen), muss der Weg eines Nutzers zu den Daten auf drei Ebenen kontrolliert werden. In der IHK-Prüfung muss man diese drei Begriffe strikt trennen können!

1. **Zutrittskontrolle (Physisch):**
   Verhindert, dass Unbefugte physisch in die Gebäude oder Räume gelangen, in denen IT-Systeme stehen (z. B. Serverraum, Büro).
   *Beispiele:* Chipkarten, RFID-Badges, biometrische Scanner, Sicherheitsschlösser, Wachdienst, Zäune.

2. **Zugangskontrolle (Systemebene):**
   Verhindert, dass Unbefugte das IT-System oder das Netzwerk an sich nutzen können (Login am System).
   *Beispiele:* Benutzername und sicheres Passwort, [[MFA, SSO, Passwortrichlinien|MFA (Multi-Faktor-Authentifizierung)]], Smartcards am Laptop, VPN-Einwahlzertifikate, Bildschirmsperre.

3. **Zugriffskontrolle (Datenebene):**
   Stellt sicher, dass ein (bereits erfolgreich im System angemeldeter) Nutzer nur die Daten lesen, schreiben oder löschen darf, für die er explizit berechtigt ist.
   *Beispiele:* NTFS-Dateiberechtigungen, [[Berechtigungskonzepte|Rollen- und Rechtekonzepte (RBAC)]], Verschlüsselung von Laufwerken, Freigabeberechtigungen.

*Eselsbrücke:* **Zutritt** zum Raum -> **Zugang** zum Rechner -> **Zugriff** auf die Datei.

Querverweise: [[TOM]], [[Schutzziele der IT]].
