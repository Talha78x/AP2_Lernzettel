# Cyber-physische Systeme Sensoren, Aktoren und Bibliotheken

Ein **Cyber-physisches System (CPS)** ist ein Verbund aus informationstechnischen und softwaretechnischen Komponenten mit mechanischen und elektronischen Teilen, die über eine Dateninfrastruktur (wie das Internet) miteinander kommunizieren. CPS sind die Grundlage von Industrie 4.0 und Smart Factories.

Die wichtigsten Bestandteile sind:
- **Sensoren:** Sie erfassen Daten aus der physischen Welt (z. B. Temperatur, Bewegung, Licht) und wandeln sie in digitale Signale um.
- **Aktoren:** Sie nehmen digitale Befehle entgegen und führen physische Handlungen aus (z. B. einen Motor starten, ein Ventil schließen oder eine LED einschalten).
- **Steuerungssoftware / Middleware:** Sie verarbeitet die Sensordaten und entscheidet, was die Aktoren tun sollen.
- **Vernetzung:** Die Kommunikation läuft oft über spezielle IoT-Protokolle wie MQTT oder klassische Netzwerkprotokolle (siehe [[Standardprotokolle TCP, UDP, MAC, ARP, ICMP, HTTP, HTTPS, FTP, SMTP....]]).

In der Praxis (und oft im Prüfungslabor) werden CPS mit Mikrocontrollern (wie ESP32 oder Raspberry Pi) realisiert. Für die Programmierung nutzt man vorgefertigte **Bibliotheken (Libraries)**, um nicht jeden Sensor von Grund auf neu programmieren zu müssen. Diese Bibliotheken stellen fertige [[Programmierparadigmen prozedural, objektorientiert, funktional, deklarativ|Funktionen oder Klassen]] bereit, um z.B. einen Temperatursensor einfach mit `readTemperature()` auszulesen.

Querverweise: [[Automatisierung]], [[APIs und REST]], [[LAN, WAN, WLAN ....]].
