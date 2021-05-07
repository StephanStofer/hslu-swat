# Evolution of Software Architecture over the Last Decades
Ansatz Unterschied Design und Architektur.

> Architektur ist Design, aber nicht jedes Design ist Architektur. Architektur repräsentierten wichtige Designentscheide. Wie wichtig der Entscheid ist, ist messbar an den Konsequenzen bzw. Kosten etwas zu ändern.
>
> -- Grady Booch

Anders als bei mechanischen Produkten

> Software skaliert nicht ökonomisch.
>
> -- Allan Kelly

Wenn das System wächst, nimmt Komplexität nicht linear sondern annähernd exponenziell zu. Mit guter Architektur kann man entgegenwirken.

## Architecture Definitions
Zwei grosse Standards von ISO und TOGAF. Beide definieren Architektur schwammig.

## Old School Architect

* Hoher Status, separate Position
* Entscheidet alleine wie die Architektur sein soll
    * Architekturen sind smart
    * Developers sind dumm
* Ivory tower syndrome - theoretisch, in Praxis nicht umsetzbar
* Powerpoint architect syndrome - nur Schrott im Powerpoint
* Conway Law - Hierarchie und Struktur der Teams soll dem SW Produkt angepasst werden. Damit das beste herauskommt. Da arbeiten wo man am besten arbeiten kann

## Architecture Kinds
Alle traditionelle Architekten wollen einen enterprise architect sein.

* Design $\rightarrow$ developer
* Application Architecture in einem Team
* Solution A mit einem Produkt
* Enterprise A in der ganzen Firma

Auch Technische Architektur

* Business Architecture
* Application Architecture
* Data Architecture
* Technical Architecture

## Standards ab 2000

* TOGAF; gute Ideen aber zu gross, man braucht zu viel Zeit
* Arc42; häufig in Deutschland
* RUP; A la SoDa zu lange Zyklen
* Hermes; offizielle Methode vom Bund auch häufig in Kantone
* IEEE; angestaubt

Bei allen gibt es gute Ideen, aber falsch verpackt (zu wenig agil). Gute Dinge rausnehmen.

## First Findings
Ziel von Architekt Kundenbedürfnisse erfüllen. Es gibt funktionale und nicht-funktionale Anforderungen. Requirementsdokumente werden widersprüchlich je grösser sie werden. Besser agil, etwas analysieren, umsetzen, testen, verbessern.

* Problem verstehen
* Lösung identifizieren
* moderne Verfahren lösen alte ab (riesen Dokumente)

## Requirements - SMART

* **S**pecific
* **M**easurable - acceptance criteria
* **A**ssignable (who will die it?)
* **R**ealistic - within a sprint
* **T**ime-related/Traeable (when should it be done?)/ Akzeptanz Test

Jedes mal SMART in Erinnerung rufen bei Anforderungen.

## Stories - INVEST

* **I**ndependent - Stories sollten nicht von anderen abhängig sind
* **N**egotioable - kein Widerspruch sein
* **V**aluable - wenn kein Wert, dann verwerfen
* **E**stimate-able - muss verstanden sein, damit man sie schätzen kann
* **S**mall - kleine Stücke an Arbeit
* **T**estable - müssen Testbar sein damit man sie abschliessen kann

## Backlog - DEEP

* **D** Detailed Appropriately
* **E** Estimated
* **E** Emergent
* **P** Prioritized

## Backlog Item
Ein Procut Backlog Item PBI ist ein edle ToDo-Liste. Keine Referenzen von Dokument auf Backlog. Ein PBI kann eine Story sein. Eine Schätzung lohnt sich nur wenn man über die Umsetzung diskutiert, wenn man es eh umsetzen muss, ist eine Schätzung nur verschwendete Zeit. Ein PBI ist fertig wenn technische und funktionale Anforderungen (User) erfüllt sind.

## DDD and Event Storming
Es ist wichtig, dass man Kundensprache (Domäne) spricht und man benötigt Fachdomänenwissen. Als Architekt muss man Workshop und Diskussionen führen. UX Workshops leiten und Design Thinking.

### Agile Approach
Vision, wieso will man das? Elevator Pitch. Wohin man in den nächsten 9-18 Monate (Roadmap). Release Planung mit Story Map. Sprint Backlog - Was macht man in den 1-2 Woche. MVP - minimum viable Product. MMP Minimum Marketable Product (nicht vergessen)

* effizienteste und effektivste Methode ist face to face Kommunikation
* die beste Architektur entsteht mit der Zeit von selbst-organisierten Teams

### Craftsmanship Approach
Ein Architekt ist ein

* Domänenexperte
* Software Craftsmanship
* Lean Leader, entwickelt sein Team - Mentor
* muss auf versch. Levels/Ebenen diskutieren können (Chef-level, Stakeholder, usw.)
