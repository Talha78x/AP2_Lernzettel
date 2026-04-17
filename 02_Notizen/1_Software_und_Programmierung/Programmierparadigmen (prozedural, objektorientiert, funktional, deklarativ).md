# Programmierparadigmen (prozedural, objektorientiert, funktional, deklarativ)

## Definition
Programmierparadigmen sind grundlegende Denk- und Strukturierungsweisen, mit denen Programme aufgebaut und Probleme gelöst werden.  
Sie prägen, **wie** Quellcode geschrieben, organisiert und verstanden wird.

## Wichtige Grundunterscheidung
- **Imperativ**: Beschreibt Schritt für Schritt, *wie* ein Ziel erreicht wird.
- **Deklarativ**: Beschreibt eher, *was* erreicht werden soll, nicht jeden Einzelschritt.

## Prozedurale Programmierung
### Merkmale
- Programme bestehen aus Prozeduren, Funktionen und Befehlsfolgen.
- Daten und Verarbeitung sind oft getrennt.
- Der Kontrollfluss steht im Vordergrund.

### Vorteile
- Einfacher Einstieg.
- Gut für klar strukturierte Abläufe.
- Häufig effizient und nah an der Maschine.

### Nachteile
- Bei großen Projekten schwer wartbar.
- Änderungen an Datenstrukturen wirken sich oft auf viele Stellen aus.

### Beispiele
- C
- Pascal

## Objektorientierte Programmierung (OOP)
### Merkmale
- Programme bestehen aus Objekten.
- Objekte kapseln Daten und Methoden.
- Wichtige Konzepte: Klasse, Objekt, Vererbung, Polymorphie, Kapselung.

### Vorteile
- Gute Strukturierung großer Anwendungen.
- Wiederverwendbarkeit.
- Bessere Wartbarkeit durch Kapselung.

### Nachteile
- Höhere Komplexität.
- Für kleine Skripte oft unnötig aufwendig.

### Beispiele
- Java
- C#
- Python (unterstützt mehrere Paradigmen)

## Funktionale Programmierung
### Merkmale
- Funktionen sind zentrale Bausteine.
- Möglichst keine Seiteneffekte.
- Unveränderliche Daten (Immutability) spielen eine wichtige Rolle.
- Rekursion ist oft wichtiger als Schleifen.

### Vorteile
- Gut testbar.
- Weniger Nebenwirkungen.
- Häufig gut für Parallelisierung geeignet.

### Nachteile
- Anfangs ungewohnt.
- Teilweise andere Denkweise als bei imperativer Programmierung.

### Beispiele
- Haskell
- Elixir
- Scala (multi-paradigm)

## Deklarative Programmierung
### Merkmale
- Das gewünschte Ergebnis steht im Vordergrund.
- Der Lösungsweg wird stärker von Sprache, Engine oder Laufzeit bestimmt.

### Beispiele
- SQL
- HTML
- Teile von Prolog

## Vergleich
| Paradigma | Fokus | Typische Stärke |
|---|---|---|
| Prozedural | Abläufe und Befehlsfolgen | Klare, lineare Programme |
| Objektorientiert | Objekte und Zustände | Große, wartbare Anwendungen |
| Funktional | Funktionen und Unveränderlichkeit | Gut testbarer, nebenwirkungsarmer Code |
| Deklarativ | Beschreibung des Ziels | Kürzere und oft ausdrucksstarke Lösungen |

## Prüfungsrelevante Punkte
- Unterschied zwischen **imperativ** und **deklarativ** erklären.
- Prozedural und objektorientiert gegeneinander abgrenzen.
- Vorteile funktionaler Ansätze benennen.
- Beispiele für Sprachen je Paradigma nennen.

## Obsidian-Links
- [[Programmiersprachen]]
- [[Algorithmen und Kontrollstrukturen]]
- [[Pseudocode]]
- [[UML Diagramme]]
- [[SQL Befehle (Aufbau, Arten und JOINs)]]


# Programmierparadigmen prozedural, objektorientiert, funktional, deklarativ

Ein Programmierparadigma ist der grundlegende Denkansatz, nach dem ein Programm strukturiert wird. In IHK-Prüfungen wird oft nach den wesentlichen Unterschieden gefragt. Man unterscheidet grob zwischen **imperativer** (Wie wird etwas gemacht?) und **deklarativer** (Was soll gemacht werden?) Programmierung.

**Imperative Paradigmen:**
1. **Prozedurale Programmierung:** 
   Das Programm wird in kleine, wiederverwendbare Unterprogramme (Prozeduren/Funktionen) aufgeteilt. Der Code wird Schritt für Schritt (sequenziell) von oben nach unten ausgeführt. Variablen und Zustände verändern sich während der Laufzeit. (Beispiel: C).
2. **Objektorientierte Programmierung (OOP):** 
   Programme werden als Sammlung von Objekten modelliert, die Eigenschaften (Attribute) und Verhalten (Methoden) besitzen. Die Blaupause für ein Objekt ist die *Klasse*. Wichtige Kernkonzepte sind Kapselung, Vererbung und Polymorphie. (Beispiel: Java, C#).

**Deklarative Paradigmen:**
3. **Funktionale Programmierung:** 
   Das Programm wird als Auswertung mathematischer Funktionen betrachtet. Ein zentrales Merkmal ist, dass Funktionen keine Seiteneffekte haben und Daten nicht verändert werden (Immutability). (Beispiel: Haskell).
4. **Logische / Deklarative Programmierung:** 
   Man beschreibt nur das Problem und die logischen Zusammenhänge (Regeln und Fakten), aber nicht den genauen Lösungsweg. Der Compiler oder Interpreter findet die Lösung selbst. (Beispiel: [[SQL Befehle Aufbau, Arten und JOINs|SQL]], Prolog).

Querverweise: [[Algorithmen und Kontrollstrukturen]], [[Programmiersprachen]], [[UML Diagramme]].

