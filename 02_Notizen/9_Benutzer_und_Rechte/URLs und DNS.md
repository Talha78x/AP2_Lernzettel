# URLs und DNS

## Definition
Eine **URL (Uniform Resource Locator)** ist die vollständige Adresse einer Ressource im Netz. **DNS (Domain Name System)** übersetzt Namen in IP-Adressen und umgekehrt.

## Warum ist das so?
Menschen arbeiten besser mit Namen wie `www.beispiel.de`, Computer brauchen aber IP-Adressen. Zusätzlich muss eine Adresse mehr enthalten als nur den Hostnamen, zum Beispiel:
- welches Protokoll genutzt wird
- welcher Pfad aufgerufen wird
- welche Parameter mitgegeben werden

Darum ergänzen sich URL und DNS.

## Zusammenspiel
- [[Netzwerkrelevante Dienste (DHCP, DNS, NTP, SNMP...)]] erklärt DNS als Infrastrukturdienst.
- [[Mail-Service (MX, A, AAAA..)]], [[Standardprotokolle (TCP, UDP, MAC, ARP, ICMP, HTTP, HTTPS, FTP, SMTP...)]] und [[TLS & SSL]] bauen darauf auf.
- [[Active Directory und LDAP]] ist in Unternehmensnetzen ebenfalls stark von DNS abhängig.

## Eigene Worte (prüfungsnah)
Die URL beschreibt die Ressource vollständig, DNS sorgt dafür, dass der Hostname darin technisch aufgelöst werden kann. Ohne DNS wäre die URL für Menschen zwar lesbar, für die Verbindung aber unpraktisch.

## Aufbau einer URL
Beispiel:
`https://www.beispiel.de:443/produkte?id=5#details`

| Teil | Bedeutung |
|---|---|
| `https` | Schema / Protokoll |
| `www.beispiel.de` | Hostname / FQDN |
| `443` | Port |
| `/produkte` | Pfad |
| `?id=5` | Query-Parameter |
| `#details` | Fragment / Anker |

## DNS-Auflösung vereinfacht
1. Client prüft lokalen Cache.
2. Client fragt den konfigurierten Resolver.
3. Falls nötig, wird rekursiv bzw. hierarchisch weiter aufgelöst.
4. IP-Adresse wird zurückgegeben und zwischengespeichert.

## Wichtige DNS-Begriffe
| Begriff | Bedeutung |
|---|---|
| Resolver | fragt Namen im Auftrag des Clients auf |
| autoritativer Nameserver | zuständig für eine Zone |
| TTL | bestimmt, wie lange Antworten gecacht werden |
| FQDN | vollständiger qualifizierter Domainname |

## Typische Prüfungsfallen
| Irrtum | Korrektur |
|---|---|
| URL und DNS sind dasselbe | nein, URL ist Adresse, DNS ist Namensauflösung |
| Fragment wird an den Server übertragen | oft nein, das ist vor allem Browser-intern |
| DNS ist nur fürs Web da | nein, viele Dienste hängen davon ab |

## Beispielaufgabe mit Lösung
**Aufgabe:** Eine Webseite ist per IP erreichbar, aber nicht über `www.beispiel.de`. Welcher Bereich ist zuerst zu prüfen?

**Lösung:**
**DNS**

**Begründung:**
Wenn der Zugriff per IP funktioniert, ist die Grundverbindung da. Wahrscheinlich liegt das Problem in der Namensauflösung oder im DNS-Eintrag.

## Typische Prüfungsszenarien
- URL-Bestandteile benennen.
- URL und DNS unterscheiden.
- DNS-Auflösung grob erklären.
- erklären, warum eine Webseite per IP, aber nicht per Namen erreichbar sein kann.

## Merksätze
- Die URL beschreibt das Ziel vollständig.
- DNS übersetzt Namen in IP-Adressen.
- Funktionierende IP-Verbindung heißt nicht automatisch funktionierendes DNS.
