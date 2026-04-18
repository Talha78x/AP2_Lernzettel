# QoS

## Definition
**QoS (Quality of Service)** bezeichnet Verfahren, mit denen Netzwerkverkehr unterschiedlich behandelt und priorisiert wird. Ziel ist, wichtige oder zeitkritische Daten trotz begrenzter Bandbreite möglichst zuverlässig und mit passender Qualität zu übertragen.

## Warum ist das so?
Ohne QoS gilt meist das **Best-Effort-Prinzip**: Pakete werden grundsätzlich gleich behandelt. Das ist für viele Anwendungen ausreichend, aber problematisch bei:
- **VoIP**
- **Videokonferenzen**
- **Livestreaming**
- zeitkritischen Steuerdaten

Diese Anwendungen reagieren empfindlich auf Verzögerungen und Schwankungen. Wenn große Downloads oder Backups dieselbe Leitung auslasten, leidet die Qualität.

## Zusammenspiel
- [[Standardprotokolle (TCP, UDP, MAC, ARP, ICMP, HTTP, HTTPS, FTP, SMTP...)]] erklärt, warum besonders UDP-basierte Echtzeitdienste von QoS profitieren.
- [[LAN, WAN, WLAN ....]] zeigt, dass QoS vor allem auf belasteten WAN- oder WLAN-Strecken wichtig wird.
- [[VPN (Tunneling, standortübergreifende Kommunikation)]] kann zusätzliche Engpässe schaffen, bei denen Priorisierung relevant wird.
- [[Anforderungen an Bandbreite, Latenz, Verfügbarkeit, Übertragungsmedien und Netzwerksicherheit]] ergänzt die betriebliche Sicht.

## Eigene Worte (prüfungsnah)
QoS macht ein Netzwerk nicht schneller. Es entscheidet nur, welcher Verkehr im Engpass bevorzugt behandelt wird. Sprachpakete können dadurch vor einem großen Dateidownload übertragen werden.

## Wichtige Qualitätsmerkmale
| Begriff | Bedeutung | Warum wichtig? |
|---|---|---|
| Bandbreite | Datenmenge pro Zeit | begrenzt, daher Konkurrenz zwischen Diensten |
| Latenz | Verzögerung bis zur Ankunft | wichtig für Sprache und Interaktion |
| Jitter | Schwankung der Verzögerung | stört Audio und Video |
| Paketverlust | verlorene Pakete | verschlechtert Qualität oder zwingt zu Wiederholungen |

## Was macht QoS konkret?
| Maßnahme | Wirkung |
|---|---|
| Klassifizierung | Verkehr wird erkannt und eingeordnet |
| Markierung | Pakete erhalten Prioritätskennzeichen |
| Priorisierung | wichtige Pakete werden bevorzugt behandelt |
| Queueing | Warteschlangen werden unterschiedlich abgearbeitet |
| Traffic Shaping / Policing | Datenraten werden geglättet oder begrenzt |

## Typische Priorisierung
| Verkehr | Priorität | Begründung |
|---|---|---|
| VoIP | hoch | sehr empfindlich gegen Latenz und Jitter |
| Videokonferenz | hoch | interaktiv und zeitkritisch |
| Webzugriffe | mittel | spürbar, aber weniger kritisch |
| Backup / FTP / große Downloads | eher niedrig | meist nicht zeitkritisch |

## Wichtige Prüfungsfalle
**QoS erhöht nicht die physische Bandbreite.**

Es sorgt nur dafür, dass im Engpass wichtige Pakete bevorzugt oder unwichtige Datenströme begrenzt werden.

## Beispielaufgabe mit Lösung
**Aufgabe:** In einer Außenstelle ruckeln VoIP-Gespräche immer dann, wenn parallel große Dateidownloads laufen. Welche Netzwerkmaßnahme ist passend?

**Lösung:**
Eine passende Maßnahme ist **QoS mit Priorisierung von Sprachverkehr**.

**Begründung:**
1. VoIP ist empfindlich gegen Latenz, Jitter und Paketverlust.
2. Downloads sind meist weniger zeitkritisch.
3. QoS kann Sprachpakete bevorzugen, sodass Gespräche stabiler bleiben.

## Typische Prüfungsszenarien
- erklären, warum QoS besonders für VoIP wichtig ist.
- QoS von bloßer Bandbreitenerhöhung unterscheiden.
- Latenz, Jitter und Paketverlust definieren.
- Beispiele sinnvoll priorisieren.

## Merksätze
- QoS priorisiert, aber beschleunigt nicht die Leitung selbst.
- Echtzeitverkehr braucht meist höhere Priorität.
- Engpässe werden durch QoS geordnet, nicht beseitigt.
