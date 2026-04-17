# Domänenkonzepte

In größeren Unternehmen (Multi-Site-Architekturen) reicht eine einzelne Domäne oft nicht aus. Active Directory bietet hier eine hierarchische Struktur.

- **Einzelne Domäne (Single Domain):** Einfachste Form. Alle Objekte in einer Domäne, ein oder mehrere Domänencontroller. Ausreichend für kleine und mittelständische Unternehmen.
- **Domänenbaum (Tree):** Mehrere Domänen in einer gemeinsamen hierarchischen Namensstruktur (z.B. `firma.local` als Root, `it.firma.local` und `sales.firma.local` als Kind-Domänen). Die Domänen vertrauen sich automatisch gegenseitig (transitives Vertrauensverhältnis).
- **Gesamtstruktur (Forest):** Der oberste Container im AD. Besteht aus einem oder mehreren Domänenbäumen. Alle Domänen in einem Forest teilen dasselbe Schema (Datenbankstruktur).
- **Sites und Replikation:** Physisch getrennte Netzwerkstandorte (z.B. Standort Berlin und München) werden als *Sites* definiert. AD repliziert Änderungen (z.B. neues Benutzerkonto) zwischen den DCs. Die Site-Konfiguration optimiert, wann und wie oft über die oft langsamen WAN-Leitungen repliziert wird.

Querverweise: [[Active Directory und LDAP]], [[Berechtigungskonzepte]].
