# Architekturen
#### 3-Schichten-Architektur - [Details](https://www.ibm.com/de-de/topics/three-tier-architecture)
Die 3-Schichten-Architektur ist eine lineare Softwarearchitektur. Alle Anfragen durchlaufen alle drei Schichten von oben bis unten.
***Schichten:***
1. **Darstellungsschicht/Benutzerschnittstelle:** Zum Beispiel die GUI oder  Weboberfläche. *Aufgaben:* Datendarstellung und Benutzereingaben entgegennehmen
2. **Logikschicht:** Beinhaltet die Businesslogik
3. **Datenschicht:** Die Datenbank

#### MCV-Pattern (Model-View-Controller) - [Details](https://www.geeksforgeeks.org/mvc-design-pattern/)
Die dreiteile MVC Architektur ist dreieckig angeordnet und sorgt für separation of concerns und  Modularität.
***Komponenten:***
- **Model:** Ist für die Daten und die Businesslogik zuständig.
- **View:** Zeigt die Daten, die es vom *Model* erhält an und schickt user input an den *Controller*. 
- **Controller:** Das Verbindungsstück zwischen *Model* und *View*. Validiert den user input und updated das *Model* und die *View*.
![[ap2-MVC.png]]

---
# Design Patterns
#### Observer - [Details](https://refactoring.guru/design-patterns/observer)
Das Observer-Pattern folgt dem Publisher/Subscriber Prinzip. Die Publisher-Klasse stellt Methoden bereit, die Subscriber-Klassen, die alle ein gemeinsames Interface implementieren müssen, nutzen können, um einen Eventstream zu abonnieren.

#### Singleton - [Details](https://refactoring.guru/design-patterns/singleton)
Das Singleton-Pattern ist dazu da, um sicherzustellen, dass es von einer Klasse nur eine Instanz existiert. Das geschieht häufig in Frameworks mit Dependency-Injection. Die manuelle Implementierung funktioniert durch einen privaten Constructor und eine [[Softwarearchitektur#Factory - [Details](https //refactoring.guru/design-patterns/factory-method)|Factory]] Methode in der Klasse um die eine Instanz zu bekommen

#### Factory - [Details](https://refactoring.guru/design-patterns/factory-method)
Eine Factory bietet Methoden zum erstellen von Instanzen einer Klasse. Dabei kann in den Factory-Methoden die Konfiguration der erzeugten Instanzen angepasst werden.

---
# Datenbanktypen

**[[Relationale Datenbank|Relationale Datenbanken]]**
Relationale Datenbanken sind in Tabellen organisiert und werden mit SQL abgerufen.

**Nicht-Relationale Datenbanken**
Nicht-relationale Datenbanken, auch NoSQL genannt basieren nicht auf Tabellen sondern weisen eigene Strukturen auf.

*Typen:*
- Key-Value Stores (z.B. Redis) können anhand des Keys abgerufen werden
- Document Store (z.B. Elasticsearch) können anhand des Keys oder der Metadaten oder des Inhalts des Documents abgerufen werden 
- Vektordatenbanken für Machine Learning und Datenclustering
- Graphdatenbanken speichern Beziehungen mit Metadaten zwischen den Daten