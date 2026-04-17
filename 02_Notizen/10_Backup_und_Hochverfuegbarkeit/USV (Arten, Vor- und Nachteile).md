# USV Arten, Vor- und Nachteile

Eine **USV** (Unterbrechungsfreie Stromversorgung) schützt sensible IT-Systeme (siehe [[Server und Storage]]) vor Stromausfällen, Spannungsschwankungen und Frequenzstörungen. Sie sichert primär das Schutzziel der [[Schutzziele der IT|Verfügbarkeit]].

In der IHK-Prüfung werden drei Hauptklassen unterschieden (nach IEC 62040-3):

**1. VFD (Voltage and Frequency Dependent) / Offline-USV / Standby-USV:**
- *Funktion:* Der Strom fließt im Normalbetrieb direkt vom Netz zum Server. Bei Stromausfall schaltet die USV in 2 bis 10 Millisekunden auf Batteriebetrieb um.
- *Vorteile:* Günstig, klein, hoher Wirkungsgrad.
- *Nachteile:* Keine Filterung von Frequenz- oder Spannungsschwankungen. Die Umschaltzeit kann für hochempfindliche Systeme (wie große Datenbank-Server) schon zu lang sein. Einsatz eher für Arbeitsplatzrechner.

**2. VI (Voltage Independent) / Line-Interactive-USV:**
- *Funktion:* Wie VFD, aber sie kann Unter- oder Überspannungen aktiv ausgleichen (Regelung), ohne gleich auf die Batterie zuzugreifen. Die Umschaltzeit liegt bei 2 bis 4 ms.
- *Vorteile:* Besserer Schutz vor Spannungsschwankungen, schont die Batterie.
- *Nachteile:* Filtert keine Frequenzschwankungen. Einsatz oft in kleineren Serverschränken.

**3. VFI (Voltage and Frequency Independent) / Online-USV / Doppelwandler:**
- *Funktion:* Der eingehende Wechselstrom wird in Gleichstrom umgewandelt (lädt die Batterie) und danach sofort wieder in perfekten Wechselstrom zurückgewandelt. Der Server hängt *immer* am künstlich erzeugten Strom der Batterie/des Wandlers.
- *Vorteile:* Perfekte Stromqualität (Filtert *alle* Störungen). **Umschaltzeit von 0 Millisekunden**, da der Server permanent über den Wandler versorgt wird. 
- *Nachteile:* Sehr teuer, lauter Lüfter, ständiger Stromverbrauch (Wärmeverlust durch Doppelwandlung). Zwingender Standard in Rechenzentren.

Querverweise: [[Notfallkonzept, Disaster Recovery]], [[Schutzziele der IT]].
