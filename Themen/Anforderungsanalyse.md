# Vorgehen
**Schritt 1: Rollen Zuweisen**
Rollen im Projekt werden zugewiesen, dazu ist auch eine [[Projektmanagement#Stakeholder-Analyse|Stakeholder-Analyse]] hilfreich.

**Schritt 2: Mit Stakeholder reden**
Was sind Ziele und Erfolgsbedingungen für das Projekt? Was macht ihnen Sorgen?

**Schritt 3: Annahmen und Anforderungen Auflisten**
Zeitplan aufstellen, Projektmitglieder festlegen, Risiken auflisten.
SMART Überprüfen

**Schritt 4: Zustimmung Einholen**
Scope Creep verhindern - Grenzen klar benennen
Von allen wichtigen Beteiligten Zustimmung einholen

---
# Funktionale vs nicht-Funktionale
**Funktionale Anforderungen:** *Was* muss die Software können?
z.B. Die Software muss den Body-Mass-Index basierend auf einer gegebenen Formel auf eine Nachkommastelle genau berechnen.

**Nicht-Funktionale Anforderungen:** *Wie* muss die Software ihre Aufgabe erledigen?
z.B.
- Zeitverhalten: “Die Anfrage muss in 10ms bearbeitet sein”
- Ressourcenverbrauch: “Bei 10.000 Anfragen pro Minute darf die CPU nur zu 50% Ausgelastet sein.”
- Robustheit: “Die Software kann 4 Wochen laufen ohne Neustart”

---
# User Stories
User Stories sind in Alltagssprache formulierte Software-Anforderungen in [[Projektmanagement#Agile Vorgehensmodelle|agilen Frameworks]].

**Struktur:** "Als *\<Rolle\>* möchte ich *\<Ziel/Wunsch\>*, um *\<Nutzen\>*"
*Beispiel:* “Als registrierter Benutzer möchte ich mein Passwort ändern können, um die Sicherheit meines Kontos zu gewährleisten.”
## Use Cases
Use Cases kommen aus der [[Projektmanagement#Klassische Vorgehensmodelle|klassischen Softwareentwicklung]] und dienen Ebenfalls der Anforderungsdarstellung in Kontext und Anwendersprache.

Ein Use Case ist aber die Bündelung aller Szenarien die bei der Benutzung der Anwendung zum erreichen eines Business Goals eintreten können.
Aus ihnen können die [[Anforderungsanalyse#INVEST-Kriterien|INVEST-Kriterien]] abgeleitet werden.

Use Cases beschreiben detailliert, wie ein Nutzer mit einem System interagiert, inklusive aller Schritte, Alternativen und Ausnahmen.

Während Use Cases umfassend und systemzentriert sind, sind User Stories kurz, nutzerzentriert und fördern die Kommunikation im Team. ​
### Ableitung von User Stories aus Use Cases
 Um daraus User Stories abzuleiten, identifiziert man die Hauptziele des Nutzers und formuliert diese in der oben genannten [[Anforderungsanalyse#User Stories|Struktur]]. 

---
# INVEST-Kriterien
Das Akronym bezieht sich auf eine User Story (U.S.) und steht für:
**I**ndependent - Die Story sollte eigenständig umsetzbar sein.
**N**egotiable - Sie ist nicht in Stein gemeißelt und kann angepasst werden.
**V**aluable - Sie liefert einen erkennbaren Nutzen für den Anwender.
**E**stimatable - Der Aufwand kann vom Team eingeschätzt werden.
**S**mall - Sie sollte in einem Sprint umsetzbar sein
**T**estable - Es lassen sich klare Akzeptanzkriterien definieren.

---
# Make-or-Buy-Entscheidungen
Um zu entscheiden, ob eine Software in-house entwickelt oder gekauft werden soll, kann wie folgt vorgegangen werden:

**Operative vs Strategische Entscheidungen**
*Operativ:* vor allem kurzfristige Ziele, z.B. Kosten oder Fristeneinhaltung
*Strategisch:* langfristige Ziele. Was soll das Unternehmen selbst machen? Wie soll es aufgestellt sein?

**Faktoren Betrachten**
- **Zielsetzung**
	- Beeinflusst die Entscheidungsfaktoren
	- z.B. Wirtschaftlich? Kosten wichtiger
- **Kosten**
    - *Make:* Material, Personal, Räumlichkeiten etc.
    - *operativ:* kurzfristige Kostenersparnis durch Kauf
    - *Buy:* Beschaffungskosten
    - *strategisch:* langfristige Kostenersparnis bei Selbstentwicklung
- **Know-How**
    - *operativ:* ist das notwendige Know-How schon vorhanden?
    - *strategisch:* möchte das Unternehmen das Know-How aufbauen?
- **Qualität**
    - *+ Make:* Interne Qualitätssicherung und Überwachung
    - *- Make:* Interner Qualitätsverlust (z.B. durch Abgang Erfahrener Mitarbeiter) könnte Projekt bremsen
- **Ressourcen**
    - Haben wir genug Ressourcen um das Projekt selbst umzusetzen?
- **Risiken**
	- *Make:* Ausfallzeiten, Personal etc.
	- *Buy:* Dienstleisterausfall, Abhängigkeit