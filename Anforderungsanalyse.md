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