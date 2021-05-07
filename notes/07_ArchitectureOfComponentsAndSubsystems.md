# Architecture of Components and Subsystems

> Ziel der Architektur ist es die menschlichen Ressourcen, die benötigt werden um die Software zu bauen oder weiterentwickeln, zu minimieren.
>
> -- Robert Martin

> Grosses Design von Beginn an ist dumm. Aber kein Design von Beginn an, ist noch dümmer.
>
> -- Dave Thomas

Das System das wir aktuell bauen, gibt es sicher gleichwertige auf der Welt. Open Source Lösungen
und Artikel ist eine ideale Quelle um an Informationen zu gelangen. Verführt zu *NIH - Not Invented
Here Syndrome*. Gebot; Kopieren, anpassen, verbessern.

## SOLID

Auf Komponentenebende gilt SOLID

* S - Single responsibility principle: hohe Kohäsion, nur ein Gurnd für Änderung
* O - Open/cloes principle: offen für Erweiterung, geschlossen für Änderungen
* L - Liskov substitution principle: jede Subklasse kann Oberklasse ersetzen
* I - Interface segregation principle: Immer Collection zurückgeben oder als Parameter erwarten (
  List und nicht ArrayList)
* D - Dependency Inversion principle: high-level Klassen sollten nicht von low-level Klassen
  abhängig sein, beide aber via Abstraktion

## Patterns

Die GoF-Pattern sind eine gute Anlaufstelle um etwas umzusetzen. Aufgeteilt in drei Teile:

* Creational
* Structural
* Behavioral

Pattern sind Lösungsvorschläge, wie wiederkehrende Probleme elegant gelöst werden können. Die
Patterns müssen für Problem evaluiert und ausgewählt werden. Patterns definieren auch eine
gemeinsame Sprache, damit man sicher besser austauschen kann.

### Builder Pattern Example

Insert code example from slides

## Layered Architecture

* Ebene-Architektur verhindert Encapsulation. Die Interfaces zwischen den Layers sind auf die
  Daten (die ausgetauscht werden) abgestimmt.
* Abstraktion wird insofern verhindert, weil nahezu jeden Layer muss alle Konzepte kennen.
* Kohäsion und Koppelung
* Law of Demeter
* Tell don't ask

//todo: add slide content

## Hexagon/Onion Architecture

Fördert Domain Models und Event-basierte Ansätze. Weiter fördert sie das Mocking von Verbinder (
Connectors), testing wird einfacher und die Integration vereinfacht

## Java Ecosystem

// todo some more stuff

* Exception Handling - runtime exceptions nutzen, Streams können checked exceptions nicht nutzen
* Für Multi Threading java.util.concurrent
* Patterns in API
* Immutability API (record)
* Java Trends (//todo research)
    * functional programming
    * immutability
    * reification
    * memory-efficiency
    * heterogeneous processors
    * fibers

## Refactor

Agressives Refactoring des Codes und Designs. Setter- wirklich nötig? Viele Setter verhindern
Multithreading. Producktentwicklung ist lernen, das Design entsprechend so gestalten, dass es
refactered werden kann. Agile meint Improvement.

### OOP Anti-Patterns

* Singletons sind schlecht
* nie `null` zurückgeben
* modifizierbare Collections nicht zurückgeben
* 