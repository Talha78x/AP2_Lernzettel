# Deploymentstrategien

Unter Deployment (Softwareverteilung / IT-Rollout) versteht man den Prozess, bei dem Software, Updates oder ganze Betriebssysteme (Images) auf Endgeräten oder Servern installiert und konfiguriert werden. Für FISIs ist dies ein typisches Projektthema.

**Rollout-Strategien:**
1. **Big Bang:** Die neue Software wird zu einem festen Stichtag unternehmensweit für alle Nutzer gleichzeitig ausgerollt.
   - *Vorteil:* Einheitlicher Stand, keine parallelen Altsysteme.
   - *Nachteil:* Sehr hohes Risiko. Wenn etwas schiefgeht, steht das ganze Unternehmen.
2. **Iterativ / Phasenweiser Rollout:** Das Deployment erfolgt schrittweise (z. B. Abteilung für Abteilung oder Standort für Standort).
   - *Vorteil:* Fehler fallen früh auf und betreffen nur eine kleine Gruppe. Geringeres Risiko.
   - *Nachteil:* Langer Zeitraum, in dem zwei Systeme (Alt und Neu) parallel betreut werden müssen (Schnittstellenprobleme).

In der modernen Softwareentwicklung (insbesondere in der Cloud) werden weitere Konzepte genutzt, z. B. **Blue/Green-Deployment** (zwei identische Produktivumgebungen, wobei der Traffic nach dem Update einfach auf die aktualisierte "Green"-Umgebung umgeschaltet wird) oder **Canary Releases** (nur ein sehr kleiner Prozentsatz der Nutzer erhält das Update zuerst).

Querverweise: [[Virtualisierung Bare-Metal, Hypervisor, Container]], [[Betriebssysteme und Anwendungen]].
