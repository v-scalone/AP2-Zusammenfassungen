
# **MVC**

Das MVC-Pattern teilt eine Anwendung in drei Hauptkomponenten:

- **Model**: Verwaltet die Daten und die Geschäftslogik. Es enthält die Funktionen, die mit den Daten arbeiten (z. B. neue Daten hinzufügen, bearbeiten oder löschen). Beispiel: In einer To-Do-App wäre das Model die Liste aller Aufgaben und die zugehörigen Funktionen (z. B. "Aufgabe hinzufügen").
- **View**: Übernimmt die Darstellung der Daten für den Benutzer und sorgt für die grafische Benutzeroberfläche (GUI). Beispiel: In der To-Do-App zeigt die View die Aufgabe als Element in der Liste.
- **Controller**: Vermittelt zwischen View und Model. Es nimmt Benutzereingaben aus der View entgegen, verarbeitet sie und kommuniziert mit dem Model, um Änderungen vorzunehmen. Beispiel: Wenn ein Benutzer auf "Aufgabe hinzufügen" klickt, informiert der Controller das Model und die View wird aktualisiert.

**Vorteil**:  
Die Trennung der Verantwortlichkeiten macht den Code modularer, wartbarer und testbarer.

---
# **Observer**

Das Observer Pattern regelt eine Beziehung zwischen einem **Subjekt** (z. B. ein Datenobjekt) und mehreren **Beobachtern** (z. B. GUIs oder Komponenten).

- Das Subjekt verwaltet eine Liste von Beobachtern.
- Wenn sich der Zustand des Subjekts ändert, benachrichtigt es automatisch alle Beobachter.

**Beispiel**: In einer Chat-App:

- Das Subjekt ist der Nachrichtenserver.
- Die Beobachter sind die Benutzer (Clients).  
    Wenn eine neue Nachricht in einem Chat eingeht, informiert der Server (Subjekt) alle Benutzer (Beobachter), damit diese die Nachricht sehen können.

**Vorteil**:  
Die lose Kopplung sorgt dafür, dass Subjekt und Beobachter unabhängig voneinander arbeiten können. Die Beobachter reagieren automatisch auf Änderungen des Subjekts.

**Alternative: Databinding**
Als Datenbindung (engl. Data Binding) bezeichnet man z. B. die automatische Weitergabe von Daten von einem Datenobjekt an ein Steuer-
elementobjekt (Viewobjekt) einer Benutzeroberfläche und umgekehrt.
(vgl. AP2, GA1 FiAE)

---
# **Factory & Abstract Factory**

Mit dem Factory Pattern wird ein Objekt über einen Methodenaufruf und nicht direkt mittels des Konstruktors erzeugt. Dies erhöht die Kapselung, da die Logik der Objekterzeugung ausgelagert wird. Ein Beispiel: In einer Onlineshop-Anwendung mit unterschiedlichen Zahlungsmethoden (z. B. PayPal, Kreditkarte, Überweisung) wird das Factory-Pattern verwendet, um flexibel auf die gewählte Zahlungsmethode zu reagieren. Unabhängig davon, welche Methode der Nutzer auswählt, kann durch einen einfachen Methodenaufruf ein Objekt des Typs "Zahlungsvorgang" erzeugt werden, ohne direkt auf spezifische Klassen oder deren Konstruktoren zurückzugreifen und spezifische Übergabeparameter ausfüllen zu müssen.

Das Abstract Factory Pattern erweitert dieses Konzept, indem es die Erstellung von ganzen Familien verwandter Objekte ermöglicht, ohne ihre konkreten Klassen anzugeben. Dies bietet noch mehr Flexibilität und ermöglicht z. B. die separate Verwaltung von Plattform- oder systemabhängigen Objekten.
Das Abstract Factory Pattern hingegen wäre geeignet, wenn du eine **Familie von verwandten Objekten** erzeugen musst. Zum Beispiel könntest du verschiedene Objekte gleichzeitig erzeugen – etwa `PayPalZahlungsvorgang`, `PayPalAuthentifizierung` und `PayPalQuittung`. Die Abstract Factory bietet dir eine Schnittstelle, um solche Objektgruppen zu erstellen, ohne auf die konkreten Klassen zu verweisen.

---
# **Singleton**

Das Singleton Pattern stellt sicher, dass von einer Klasse nur eine einzige Instanz existiert, die global in der ganzen Anwendung zugänglich ist. Es wird häufig z. B. bei der Verwaltung von Datenbankverbindungen eingesetzt.

**Vorteile**:
Die gesamte Anwendung verwendet dieselbe Instanz, wodurch nur ein einziges Objekt die Verbindung zur Datenbank herstellt.
Das spart Ressourcen, da nicht für jede neue Verbindung ein weiteres Objekt erzeugt wird.Das Schließen der Verbindung wird ebenfalls vereinfacht, da auf die globale Instanz der Singleton-Klasse zugegriffen werden kann. Dadurch entfällt die Notwendigkeit, mehrere Verbindungen manuell zu schließen.

---
# **Builder**

Das Builder Pattern wird verwendet, um komplexe Objekte Schritt für Schritt zu erstellen. Statt einen Konstruktor mit vielen Parametern zu verwenden, wird ein Builder genutzt, der das Objekt in logisch getrennten Schritten zusammenstellt.

- Der Builder bietet Methoden, um einzelne Eigenschaften eines Objekts festzulegen.
- Sobald alle Einstellungen vorgenommen wurden, erstellt der Builder das endgültige Objekt.

**Beispiel**: Beim Konfigurieren eines Autos in einem Online-Shop:

- Der Builder erlaubt dir, schrittweise Eigenschaften zu definieren (z. B. Farbe, Motor, Innenausstattung).
- Sobald alle Teile ausgewählt wurden, erstellt der Builder das fertige Auto-Objekt.

**Vorteil**:  
Das Muster sorgt für klare und übersichtliche Erstellung komplexer Objekte. Es macht den Code besser lesbar und vermeidet lange Konstruktoraufrufe mit vielen Parametern.

---
# **Prototype**

Mit dem Prototype Pattern können neue Objekte erstellt werden, indem ein Prototyp (d. h. ein bestehendes Objekt) dupliziert wird. Dies geschieht über Klonen.

- Ein Prototyp enthält alle vorhandenen Eigenschaften eines Objekts.
- Beim Klonen entsteht ein neues Objekt mit denselben Eigenschaften wie der Prototyp. Änderungen am Klon beeinflussen den ursprünglichen Prototyp nicht.

**Beispiel**: In einer Zeichenanwendung:

- Du hast ein Objekt (z. B. ein Rechteck) mit einer bestimmten Farbe, Größe und Position.
- Durch Klonen kannst du mehrere identische Rechtecke erstellen, die du unabhängig voneinander verändern kannst.

**Vorteil**:  
Das Muster spart Ressourcen, da das Klonen oft schneller ist als das wiederholte Erzeugen eines neuen Objekts von Grund auf. Es wird häufig bei sich wiederholenden Objekttypen eingesetzt.
