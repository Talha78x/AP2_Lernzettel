# APIs und REST

Eine **API** (Application Programming Interface) ist eine Programmierschnittstelle. Sie ermöglicht es zwei voneinander unabhängigen Software-Anwendungen, standardisiert miteinander zu kommunizieren und Daten auszutauschen, ohne dass die eine Anwendung den internen Quellcode der anderen kennen muss.

**REST (Representational State Transfer):**
REST ist ein spezieller, extrem weit verbreiteter Architekturstil für Webservices. Eine API, die diesen Regeln folgt, nennt man eine *RESTful API*.

Die wichtigsten Merkmale von REST für die IHK-Prüfung:
- Die Kommunikation läuft in der Regel über HTTP (bzw. verschlüsselt über HTTPS, siehe [[Standardprotokolle TCP, UDP, MAC, ARP, ICMP, HTTP, HTTPS, FTP, SMTP....]]).
- REST nutzt Standard-HTTP-Methoden für die sogenannten CRUD-Operationen (Create, Read, Update, Delete):
  - **GET:** Daten vom Server abrufen (Read).
  - **POST:** Neue Daten auf dem Server anlegen (Create).
  - **PUT / PATCH:** Vorhandene Daten ändern (Update).
  - **DELETE:** Daten löschen (Delete).
- REST ist *zustandslos* (stateless): Der Server speichert keinen Sitzungsstatus zwischen zwei Anfragen des Clients; jede Anfrage muss alle nötigen Informationen (z.B. Authentifizierungstoken) enthalten.
- Die Nutzlast (Payload) wird meist als JSON oder XML übertragen (siehe [[Dateiaustauschformate CSV, JSON, XML ....]]).

Querverweise: [[OpenData]], [[Skript- und Shellprogrammierung]].
