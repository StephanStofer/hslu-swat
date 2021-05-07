# Agile Architecture

Jeder SW Developer ist ein Designer *und* Architekt. Die Summe der gesamten Source Codes ist das
wahre Design und Architektur. Die Architektur evolviert jeden Tag, wird besser oder schlechter, wenn
Leute programmieren. Master Programmierer beeinflussen die Architektur. Wenn ein Architekt nicht
programmiert ist man weg vom Fenster. Jeder Developer ist ein Architekt, jeder sollte entsprechend
ausgebildet werden.

## Agile Architecture Prinzipien (SAFe)

1. Design entwickelt sich, Architektur ist Zusammenarbeit
1. Je grösser das System, je länger der Weg
1. Bilde die einfachste Architektur die geeignet ist
1. Wenn man Zweifel hat, coden oder modellieren
1. man entwickelt, testet und betreiben es
1. es gibt kein Monopol auf Innovation - jede Person hat gute Ideen
1. Architekturfluss implementieren

## Agile Architecture

Die Struktur (Anzahl Teams) der Firma wird sich in der Architektur widerspiegeln (z.B. mehr Teams
mehr Services).

1. Impact of Agile on Architecture
1. Decisions at the right time
1. Evolutionary Design - SW läuft oft Jahrzehnte -> auch die Daten!!
1. Architect as Coach
1. Patterns for Agility
1. Documentation

![Agile Manifesto](images/agile-manifesto.png){width=90%}

### Pain Points

Wie schnell kann man reagieren? Schnelle Änderungen/Deploys ermöglichen. Müssen einfach
verifizierbar sein. Jederzeit Lauffähig

![Pain Points](images/painpoint.png)

### Entscheidungen

* Team: junges Team gibt andere Architektur als mit alten Hasen
* RoI: früh auf den Markt, auch wenn noch nicht alle Features vorhanden - Mut zur Lücke!
* Defer with abstractions: nach hinten schieben in der Timeline, erst einführen wenn wirklich nötig
* keine Sackgassen wählen (Kulturen, Programmiersprachen, wenig Fachleute in Region, usw.)

![Entscheidungen](images/decisions.png)

### Product Backlog

Man muss Entscheide identifizieren und treffen. Je nach Wünsche von Kunden und PO, daraus entwickelt
sich Architektur. Architekt entscheidet anhand Backlog.

![Backlog](images/backlog.png)

### Quality Tree

Identifiziert Tradeoff was ist möglich, was will man (Strategie). Entscheide dokumentieren

![Quality Tree](images/qualitytree.png)

### Factors to decide

Entscheide abhängig von Fähigkeiten von Team treffen. Keine Sackgassen wählen

![](images/deadend_team.png)

### Spike

Was will ich erreichen?

![Spike](images/spike.png)

### Wichtige Liste um Architektur zu verbessern

Keine Garantie für Vollständigkeit

2. Charactersset, Mehrsprachigkeit
6. Journaling, rechtliche Aspekte absichern (logs)
9. alte Daten auch mit neuem System/Version lesbar?

![Checkliste / wichtige Fragen zur Architektur](images/checklistearchitecture.png)

### Requirements Engineering

Kriterien für Architektur ergeben sich aus Anforderungen, System muss aufgeteilt werden.

Bounding Box definieren, für jede beste Lösung suchen

![Requirements Engineering](images/re.png)

### Vision

Entscheide machen die in diese Richtung gehen. Dead-End-Entscheide vermeiden. Lernen, entscheiden,
umsetzen. Plan B in Schublade haben

![Vision](images/vision.png)

### Minimale Solution

klein anfangen
![Minimal Solution](images/minimal-solution.png)

### Architecture Workshop

Regelmässige Workshops machen Automatisches Deployment um schnelles Feedback zu erhalten Review wenn
etwas nicht autom. Testbar
![Architecture Workshop](images/workshops.png)

### Define Evolution Steps

Soll in einer Iteration umsetzbar sein.
![Define Evolution Steps](images/DefineEvolutionSteps.png)

### Architect Skills

Skills, Aufgaben, Herausforderungen und Voraussetzungen eines Architekts
![Skills of a Architect](images/architect.png)

### Agile Architectures Pattern
* Ideen wie SOLID, KISS
* Austauschbarkeit vorsehen
![Agile Architectures Pattern](images/aa-pattern.png)
  
### Identify Bounded Context

![Identify Bounded Context](images/identifybc.png)

### Documentation
Spezifikation ist wie das System gebaut ist ?? //todo: check in lecturer


![Documentation](images/documentation.png)