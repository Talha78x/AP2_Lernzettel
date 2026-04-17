# Load Balancing

Ein Load Balancer verteilt eingehende Anfragen (z.B. HTTP/HTTPS-Webzugriffe) auf mehrere dahinterliegende Server, um Überlastung zu vermeiden und die Ausfallsicherheit zu erhöhen.

**Algorithmen:**
- *Round Robin:* Anfragen werden einfach reihum auf alle Server verteilt (1→2→3→1→2→3...). Simpel, aber ohne Berücksichtigung der tatsächlichen Serverlast.
- *Least Connections:* Eine neue Anfrage geht immer an den Server mit den aktuell wenigsten aktiven Verbindungen. Intelligenter als Round Robin.
- *IP-Hash:* Ein Client wird anhand seiner IP-Adresse immer an denselben Server geleitet (Session Persistence / Sticky Sessions). Wichtig bei Webanwendungen, die Session-Daten lokal speichern.

**Layer:**
- *Layer 4 Load Balancer:* Verteilt Pakete anhand von IP-Adresse und TCP/UDP-Port, ohne den Inhalt zu verstehen.
- *Layer 7 Load Balancer (Application Delivery Controller):* Versteht HTTP. Kann z.B. anhand der URL entscheiden (`/api/...` geht zu API-Servern, `/images/...` geht zu Storage-Servern).

Querverweise: [[Snap-Shot, Versionierung, Hochverfuegbarkeit Clustering, Load Balancing, FHRP]], [[Netzwerkkomponenten]].
