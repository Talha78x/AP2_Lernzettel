# Security by Design

**Security by Design** (und das eng verwandte **Privacy by Design**) bedeutet, dass IT-Sicherheit und Datenschutz nicht erst am Ende der Software- oder Systementwicklung "daraufgebaut" werden, sondern von der ersten Konzeptphase an integraler Bestandteil der Systemarchitektur sind.

Wenn ein FISI ein neues Netzwerk oder System entwirft, bedeutet das in der Praxis:
- **Least Privilege (Minimales Rechteprinzip):** Ein Benutzer oder Dienst bekommt standardmäßig nur die Rechte, die er für seine Arbeit zwingend benötigt.
- **Fail Secure:** Wenn ein System abstürzt oder ein Fehler auftritt, geht es in einen sicheren Zustand über (z.B. eine Firewall blockiert bei Absturz allen Traffic, statt alles durchzulassen).
- **Defense in Depth (Tiefenverteidigung):** Sicherheit wird auf mehreren Schichten aufgebaut (z.B. äußere Firewall, innere Netzsegmentierung über [[VLAN Arten, Trunking ....|VLANs]], Host-Firewall, Verschlüsselung auf Laufwerksebene). Fällt eine Schicht, hält die nächste.
- **Privacy by Default:** Die datenschutzfreundlichsten Einstellungen sind die Voreinstellung (Nutzer müssen unsichere oder datensammelnde Funktionen aktiv *einschalten*).

In Prüfungen wird dieser Ansatz oft als moderne und kosteneffiziente Alternative zum reinen "Reagieren auf Angriffe" abgefragt, da nachträgliches Härten von Systemen oft sehr teuer oder fehleranfällig ist.

Querverweise: [[Schutzbedafsanalyse und Riskoanalyse]], [[Berechtigungskonzepte]], [[DSGVO und IT-Grundschutz Personbezogene Daten usw...]].
