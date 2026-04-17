# RADIUS und AAA

**AAA** steht für **Authentication, Authorization und Accounting** – das Drei-Säulen-Modell der zentralen Zugangskontrolle.

1. **Authentication (Authentifizierung):** Wer bist du? (Identitätsprüfung, z.B. per Zertifikat oder Passwort).
2. **Authorization (Autorisierung):** Was darfst du? (Welche Netzwerkbereiche darf dieser Benutzer nutzen?).
3. **Accounting (Abrechnung/Protokollierung):** Was hast du gemacht? (Lückenlose Protokollierung von Login-Zeiten, genutzten Ressourcen).

**RADIUS (Remote Authentication Dial-In User Service) – Port 1812/1813 UDP:**
Das am häufigsten eingesetzte Protokoll zur Realisierung von AAA.
*Typischer Einsatzfall:* Ein Mitarbeiter verbindet sein Notebook mit einem WLAN-Access-Point (802.1X / EAP). Bevor das Gerät Netzwerkzugriff bekommt, fragt der Access-Point bei einem zentralen RADIUS-Server nach: "Darf dieses Gerät/dieser Benutzer rein?" Der RADIUS-Server prüft die Anfrage gegen das [[Active Directory und LDAP]] und gibt dem Access-Point ein Ja oder Nein zurück.

Querverweise: [[MFA, SSO, Passwortrichlinien]], [[Firewall (IDS, IPS, DMZ, ACL, Filtertabelle)]], [[Netzwerkrelevante Dienste (DHCP, DNS, NTP, SNMP...)]].
