# Errors, Vulnerabilities, Smells

Code muss stetig bearbeitet werden, um die Qualität zu halten.

## Clean Code

Tools nutzen um Source Code verbessern. Werkzeuge sind günstig, schnell und benötige keine grosse
Koordination. Tools finden aber nur **Fehler**, Qualität können es nicht beurteilen. Es ist ein
Mindset, jeden Tag systematisch sich verbessern.

* Compiler Fehler müssen behoben werden
* Compiler Warning auch, es gibt wenige Ausnahmen
* Statische Fehler
    * Bugs, hohe Wahrscheinlichkeit für Crash (Tool Spotbug)
    * Errors, es kann Crash
    * Vulnerabilities, Hackbar
    * Smells, Wartung wird teuerer

### Tools für CC

* Analyzer in IDE
* Jacoco
* SpotBugs
* SonarLint and SonarQube
* Checksyle (Historisch)
* PMD (Historisch)

#### Sonar Rules

Enthält mehr als 500 Regeln, Enthält Subset von OWASP Vulnerabilities, defacto Standard.

Das Ziel Qualität des Produktes steigern und somit auch Source Code.

#### OWASP

* Injection
* Broken Authentication
* Sensitive Data Exposure
* XML External Entities XEE
* Broken Access Control
* Security Misconfiguration
* Cross Site Scripting XSS
* Insecure Deserialization
* Using Components with known vulnerabilities
* Insufficient Logging and Monitoring

### Why Tools

* sind günstiger als ein Review durch Personen
* man kann es jede wenige Minuten machen
* Niemand schaut über die Schulter
* finden nur einfache Probleme

### Ziele

* keine Compiler Errors
* keine Compiler Warnung
* keine Sonar, Spotbugs errors, Vulnerabilities or smells
* Code Coverage sollte höher als 60% sein
* **Jeder gefundene Bug erhält ein Test, welcher den Fehler reproduziert, bevor der Fehler behoben
  wird**

## Why Pair Programming

Werkzeuge finden nur einfache sematische Probleme. Andere Menschen helfen das Design und Archikektur
zu verbessern. Mehrere Personen kennen den Code.

> **Wisdom of the crowd**
> Pair Programming, Mob Programming

### Next Stage - Mob Programming

Ganzes Team arbeitet zusammen um ein Problem zu lösen. Kompromiss zwischen Kosten und Zykluszeit.

> **Wisdom of the crowd**

### Technical Meetings / Dojos

Weil Tools Qualität nicht bzw. nur teilweise steigert. Coding Dojos, oder Architectur-Workshop
abhalten. Zum Beispiel nach jedem Sprint.

### SonarLint and SonarQube

* Die beiden Tools machen ein Tool
* Analyze mit SonarLint ausführen
* Generierten Report lesen
* Regelbeschreibung studieren
* wiederholen

## Forensics Approach

* Codescene
* `git log --pretty=format: --name-only | sort | uniq -c | sort -rg | head -10`
* `git log --numstat --pretty=format:'[%h] %an %ad %s' --date=short`

## Advanced Tools

* Modul-Konzepte nutzen
* [ArchUnit](https://www.archunit.org/) - Dependencyregel (Naming, usw.) als UnitTests

### Module

Hat grossen Einfluss auf Architektur. Formalisiert Boundend Domains. Compiler Validation. Für
kleinere Software Module in Monolith aufbauen.

### ArchUnits

Guter Ansatz bevor Module. Benutzerdefinierte Reegeln für spezifische Nutzen. Manchmal zögernde
Umsetzung von Features aus Java.

### DevOps Approach

Tools machen nur Sinn, wenn in CI/CD eingebunden, idelerweise Teil von Gradle/Maven. Quality-Gates
ist die logische Konsequenz.

## Zero Bug Policy

Es gibt keine offene Bugs (wenn dann terminiert). Korrigieren (jetzt!) oder verwerfen (löschen). Es wird nur Qualität
geliefert. Dadurch nur glückliche Benutzer. Kein Bug-Board mehr nötig. Kein Diskussion über Bugs,
entweder werden sie gefixt oder gelöscht.

Das Pflegen von Bugs über Monate macht keinen Sinn.

## Bad API's

* Kunden werden gezwungen schlechten Code zu schreiben
* Namenskonvention ist nicht konsistent
* Zentraler Zugang zu Features in einzelner Klasse
* keine immutable Objekte werden genutzt
* nicht dokumentierte API
* Verwendung von alter Code-Style (for-Loops anstatt streams)

## Bad Scrum / Agile

* Definition of Done fehlt
  * Bsp: in Git eingecheckt und kompiliert
* Git Training fehlt
* Coding Guidelines fehlen
* Application wird nicht mehrmals pro Woche deployt
* fehlende DevOps-Disziplin