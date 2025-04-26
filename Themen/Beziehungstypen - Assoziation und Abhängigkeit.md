
![[Pasted image 20250420145445.png]]


**Vererbung**

- **Einfach:**  
    _Eine Klasse übernimmt Eigenschaften und Methoden einer anderen Klasse._
- **Im Klassendiagramm:**  
    Wird durch einen offenen Pfeil mit einer leeren Spitze dargestellt (`△-Pfeil`), der von der Kindklasse („Subklasse“) zur Elternklasse („Superklasse“) zeigt.
- **Beispiel:**  
    Klasse `PKW` erbt von `Fahrzeug`.

---

**Assoziation**

- **Einfach:**  
    _Beschreibt eine Beziehung oder Verbindung zwischen zwei Klassen._
- **Im Klassendiagramm:**  
    Dargestellt als eine gerade Linie zwischen den Klassen.
- **Beispiel:**  
    Ein `Kunde` bestellt ein `Produkt`.

---

**Gerichtete Assoziation**

- **Einfach:**  
    _Eine einseitige Beziehung – nur eine Klasse „kennt“ die andere._
- **Im Klassendiagramm:**  
    Linie mit einem einfachen Pfeil (`→`) zum Ziel.
- **Beispiel:**  
    Eine `Schule` kennt ihre `Lehrer`:

---

**Multiplizität / Kardinalität**

- **Einfach:**  
    _Gibt an, wie viele Objekte einer Klasse mit Objekten einer anderen Klasse in Beziehung stehen können._
- **Im Klassendiagramm:**  
    Zahlen oder Bereichsangaben an den Enden der Beziehungslinie, z.B. `1`, `0..*` (beliebig viele), `1..5`.
- **Beispiel:**  
    Ein `Kunde` kann viele `Bestellungen` aufgeben, eine Bestellung gehört zu genau einem Kunden.

---

**Aggregation**

- **Einfach:**  
    _„Hat-ein“-Beziehung: Ein Objekt besteht aus anderen Objekten, die aber eigenständig bleiben können._
- **Im Klassendiagramm:**  
    Linie mit einer weißen Raute (`◊`) an der Seite des Ganzen (Container).
- **Beispiel:**  
    Eine `Mannschaft` aggregiert `Spieler`:

---

**Komposition**

- **Einfach:**  
    _Starke Form der Aggregation: Teile existieren nur, solange das Ganze existiert._
- **Im Klassendiagramm:**  
    Linie mit einer ausgefüllten Raute (`◆`) an der Seite des Ganzen.
- **Beispiel:**  
    Ein `Haus` besteht aus `Zimmern`, die ohne das Haus nicht existieren:

---

**Implementierung**

- **Einfach:**  
    _Eine Klasse übernimmt die Vorgaben (z. B. Methoden) eines Interfaces (Schnittstelle)._
- **Im Klassendiagramm:**  
    Strichlierte Linie mit offener Pfeilspitze (`---△`).
- **Beispiel:**  
    Klasse `Auto` implementiert das Interface `Fahrbar`.

