# Active Directory und LDAP

Das **Active Directory (AD)** ist Microsofts zentraler Verzeichnisdienst für Windows-Domänen. Es ist der "Herzschlag" einer Windows-Enterprise-Umgebung und speichert alle Informationen über Benutzer, Computer, Gruppen und Richtlinien.

**Kernkonzepte des AD:**
- **Domain:** Die grundlegende Verwaltungseinheit (z.B. `firma.local`).
- **Domänencontroller (DC):** Der Server, der das AD hostet und Authentifizierungen (via Kerberos-Protokoll) durchführt.
- **Organizational Units (OUs):** Ordner innerhalb des ADs, um Objekte (Benutzer, Computer) logisch zu gruppieren und unterschiedliche Gruppenrichtlinien (GPOs) anzuwenden.
- **GPO (Group Policy Object):** Regeln, die automatisch auf alle Computer oder Benutzer einer OU angewendet werden (z.B. Sperrung des USB-Ports, Passwort-Mindestlänge, Hintergrundbild).

**LDAP (Lightweight Directory Access Protocol) – Port 389 (LDAPS: 636):**
Das Protokoll, über das mit dem Active Directory (und anderen Verzeichnissen) kommuniziert wird. Wenn sich ein Benutzer einloggt, fragt sein Computer per LDAP beim DC an, ob die Zugangsdaten stimmen. LDAP ist das "Sprache" des ADs.

Querverweise: [[Domänenkonzepte]], [[Berechtigungskonzepte]], [[MFA, SSO, Passwortrichlinien]].
