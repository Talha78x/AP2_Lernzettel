# Berechtigungskonzepte

Das Konzept der Zugriffsrechte ist eng mit dem Schutzziel der Vertraulichkeit (siehe [[Schutzziele der IT]]) verbunden und in der IHK-Prüfung häufig Thema.

**Grundprinzipien:**
- **Least Privilege (Minimalprinzip):** Jeder Benutzer und jeder Prozess erhält nur die Berechtigungen, die er für seine Aufgaben zwingend benötigt – nicht mehr.
- **Need-to-Know-Prinzip:** Ergänzend zum Least-Privilege-Prinzip: Informationen werden nur an diejenigen weitergegeben, die sie für ihre Arbeit benötigen.

**Berechtigungsmodelle:**
- **DAC (Discretionary Access Control):** Der Eigentümer einer Ressource (z.B. einer Datei) entscheidet selbst, wer darauf zugreifen darf. Typisch für NTFS-Dateiberechtigungen unter Windows.
- **MAC (Mandatory Access Control):** Ein zentraler Administrator definiert Sicherheitsklassen (z.B. "geheim", "vertraulich"). Nutzer können Berechtigungen nicht selbst ändern. Wird z.B. in militärischen Systemen eingesetzt.
- **RBAC (Role-Based Access Control):** Berechtigungen werden nicht direkt Nutzern, sondern **Rollen** zugewiesen. Ein Nutzer bekommt eine Rolle (z.B. "Buchhaltung") und erbt damit alle Rechte dieser Rolle. Standard in [[Active Directory und LDAP]]-Umgebungen via Gruppen.

Querverweise: [[Zutritts-, Zugangs- und Zugriffskontrolle]], [[Active Directory und LDAP]], [[MFA, SSO, Passwortrichlinien]].
