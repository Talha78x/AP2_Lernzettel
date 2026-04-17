# MFA, SSO, Passwortrichlinien

Passwörter allein sind kein ausreichender Schutz mehr. Moderne Authentifizierungskonzepte setzen auf mehrere Schichten.

**MFA (Multi-Faktor-Authentifizierung):**
Beim Login müssen mindestens **zwei** unabhängige Faktoren aus verschiedenen Kategorien nachgewiesen werden:
1. *Wissen:* Passwort, PIN.
2. *Besitz:* Smartphone (TOTP-App wie Google Authenticator), Hardware-Token (YubiKey), Smartcard.
3. *Sein (Biometrie):* Fingerabdruck, Gesichtserkennung.
→ Selbst wenn ein Passwort gestohlen wird (z.B. durch Phishing), kann ein Angreifer ohne den zweiten Faktor nicht einloggen.

**SSO (Single Sign-On):**
Ein Benutzer meldet sich **einmal** an (z.B. an der Windows-Domäne) und hat dann Zugriff auf alle verbundenen Dienste, ohne sich erneut authentifizieren zu müssen. Technisch umgesetzt über Protokolle wie **Kerberos** (intern) oder **SAML / OAuth2 / OpenID Connect** (Web/Cloud).

**Passwortrichtlinien (via GPO):**
- Mindestlänge (z.B. 12 Zeichen).
- Komplexitätsanforderungen (Groß-/Kleinschreibung, Sonderzeichen).
- Maximales Passwortalter (z.B. alle 90 Tage ändern).
- Passwort-History (die letzten 5 Passwörter dürfen nicht wiederverwendet werden).
- Account-Sperrschwelle (nach 5 Fehlversuchen wird der Account gesperrt).

Querverweise: [[Berechtigungskonzepte]], [[Active Directory und LDAP]], [[RADIUS und AAA]].
