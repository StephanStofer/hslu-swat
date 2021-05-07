# Architecture Documentation

Die Geschichte sollte auch in die Dokumentation einfliessen, wieso gewisse Entscheide gefällt
wurden.

## Truths

* Source Code ist die Architektur
* es ist teuer und aufwändig die Dokumentation mit dem SourceCode zu synchronisieren
* bei Agile geht es um Menschen, deren Interaktionen, Stories und Diskussionen nicht über Prozesse
  und Werkzeuge
* ATAM, TOGAF, IEEE-SW sind veraltet und obsolet
* Traditionelle PM-Standards wie Hermes, Prince2 und PMI sind archeologischer Natur
* nie Word nutzen, es ist proprietär und kann nicht in VCS integriert werden
* je mehr Textdokumente, umso mehr Synchronisierungsfehler können es geben.
* Papier ist nutzlos

## Why Should You Document

Es sollte kommunikativ und informativ sein und auf Leser angepasst. Erklärungen sollten überwiegen,
anstatt korrekte formelle Notation. Kritische Informationen enthalten. Erklärende Einschränkungen
des Systems. Einfachheit der Schönheit vorziehen. Erkenntnisse und/oder Kausalitätsketten sind
relevant nicht Meinungen.

### Domain Driven Models

* Code ist Dokumentation
* Kleine Modelle mit Erklärungen
* Event Diagramme
* Akzeptanztest Reports
* Verfolgbarkeit zwischen Code, Tests und dazugehörigen Anforderungen

### UML for small Models

PlantUML! Oder mindestens Textbasiert, damit in VCS verwaltbar.

#### C4 Model for Systems

Variante von Dude auf youtube. Sagt dass Overview unbedingt graphisch dokumentieren - ist eher
statisch, gibt Überblick. Lohnt sich also. Rest nur wenn wirklich nötig.

1. SW Arch is not about Big Design up-front
1.

**Vorgehen**

1. Overview first

- System Context (Schnittstellen nach aussen)
- Containers (grosse Blöcke der Applikation, wegen untersch. Technologie oder Verteiltes System) (
  oft Docker)

1. Zoom and Filter

- Komponenten (Module (Java))

1. Detail on demand

- Klassen

## Architectural Design Record

Der ADR ist ein Dokument wieso Entscheide gefällt wurden. Inklusive Kontext und Gründe die zum
Entscheid gefüllt haben. Die Geschichte gehört zum Model und kann in die Versionkontrolle
hinzugefügt werden.

## Rules for Documentation

Nur stabile, implementierte Konzepte erfassen. Keine spekulativen Ideen. *Lebende* Dokumentation
sind berreichernd, kollaborativ und benötigen oft weniger Pflege. Siehe auch www.javadoc.io

Dokumentation sollte simple, aber nicht zu simpel verfasst sein. Aufwand und Ertrag muss stimmen,
auch beim Einsatz von Tools (Lizenzen).

Informationen öffentlich und zentral zur Verfügung stellen. Es sollte durchsuchbar sein!

## Acceptance Tests

Jede Story oder Anforderung sollte Akzeptanzkriterien haben welche mit Acceptanztests verifiziert
werden. Akzeptanzkriterien ist eine ausführbare Spezifikation und immer aktuell. Hier ist die
Tracability implizit

## Fitness Functions

Automatisch Tests für non-functional Requirements, Reporte bestätigen die Validation von allen
non-functional Requirements. Traceabilitty ist implizit.

## API Documentation

* JavaDoc
* Teil einer statischen Website
* Integriert in moderne IDE

## Configuration as Code

Jeder Askept des Systems sollte als Source Code gehandhabt werden, alles ist unter Git. Die
Traceability ist implizit gegeben und auch auditfähig.

## Static Web Sites

* Hugo, Jenkyll
* Docsy plugin für Hugo
* Pages für Github, Gitlab, Bitbucket
* JavaDoc als  Teil der  statischen Website
* Synchronisiert mit git-Repo
* Published täglich
