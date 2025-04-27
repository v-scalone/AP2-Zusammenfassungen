# Testkonzepte
**WhiteBox Testing** - Unit Testing
→ Test mit wissen über den kompletten zu testenden Quellcode.
→Die Testfälle werden aus dem Code selbst her geleitet, nicht aus den Softwarespezifikationen/Anforderungen.
→ Testen von Teilkomponenten
→ Werden von Entwicklungsteam geschrieben
→ Zeilenüberdeckungstests

**GreyBox Testing**
→ Mischung von Black und White Box

**BlackBox Testing** - E2E Testing
→ Test ohne wissen über den Quellcode
→ Die Testfälle werden aus der Softwarespezifikation hergeleitet
→ Testen des Kompletten Systems auf richtiges Ergebnis
→ können von dediziertem QA Team durchgeführt werden
→ [[Testing, Betrieb & Open Source#Äquivalenzklassenbildung|Äquivalenzklassenbildung]]
→ [weitere Infos, Äquivalenzklassenbildung](https://qcademy.de/aequivalenzklassenbildung-2/)

**Last- & Performance-Tests**
→ Zählen zu Systemtests

**Testpyramide: E2E/System - Integration - Unit**
![[ap2-testpyramide.jpg]]
Im E2E Test wird nichts gemockt!
Heißt es gibt zwei Welten, da im Unit-Test durchaus viele Zustände gemockt werden können. Somit kann ein Zustand entstehen im Unit-Test der nur da testbar ist! Um die Qualität der Software zu gewährleisten muss daher auf die Test-Pyramide geachtet werden. Genug Unit-Tests und gezielte E2E-Tests.
E2E-Tests sind aufwändiger zu gestalten und auch teurer, weil für einen E2E-Test die gesamte Anwendungslogik laufen muss. Vom Frontend, über das Backend bis hin zum Datenbankserver z.B.. Erst wenn alle erforderlichen Komponenten für die Anwendung laufen kann ein E2E-Test stattfinden.

Beispiel:
In einer Anwendung existieren Nutzer. Ein Nutzer war 2 Jahre lang inaktiv. Die Anwendungslogik besagt das inaktive Nutzer die sich wieder einloggen zuerst eine Email zum Authentifizieren bekommen.
Diese Logik ist in einem E2E-Test sehr schwer abzutesten, da ein E2E-Test keine Einsicht in die "inaktiv"-Logik hat.
Ein Unit-Test hingegen kann einen Testnutzer erstellen, das Datum der Erstellung auf vor 2 Jahre mocken und darauf dann einen Unittest durchführen.
In diesem Beispiel ist eine "inaktiv"-Logik nur wirklich von einem Unittest abzutesten. Ein E2E-Test könnte nur abtesten ob eine Authentifizierung-Email verschickt oder angekommen ist.

#### Anweisungs- und Zweigüberdeckungstests
Diese Tests dienen dazu, die Testabdeckung durch Unittests zu messen.

**Anweisungsüberdeckungstests**
Sie testen jede Anweisung im Code mindestens ein mal. Dann ist vollständige Anweisungsüberdeckung erreicht. Sie werden selten als Hauptwerkzeug in einem Vollständigkeitstest angewendet weil sie zu schwach sind.

**Zweigüberdeckungstests**
Sie testen jeden Zweig im Code mindestens ein mal. Somit sind mehr Testfälle notwendig für vollständige Abdeckung.

*Beispiel:*
```java
String output = "Hello World!";
if (x > y) {
	output = "Hello Mom!";
}
System.out.println(output);
```
Um die vollständige Anweisungsüberdeckung zu erreichen ist nur ein Test Notwendig.
Um die Vollständige Zweigüberdeckung zu erreichen werden zwei Tests benötigt. 
(`x > y` und `x < y`)

#### Äquivalenzklassenbildung
Beim Black-Box-Testing kann es Sinn machen, sich gleich Verhaltende Eingaben in Äquivalenzklassen zu Gruppieren. Diese sollten sich im Zusammenhang des Testes gleich verhalten.

**Beispiel**: Test einer Alterskontrolle für Alkoholkauf
*Äquivalenzklassen*:
- unter 16 Jährige → kein Verkauf
- 16 und 17 Jährige → nur Bier und Wein
- 18+ → alles

---
# CI/CD
CI/CD erhöht die Entwicklungsgeschwindigkeit und verringert menge der Bugs und Probleme bei der Bereitstellung der zu entwickelnden Software. Live-Systeme können laufend geupdated werden.

**Continuous Integration**
Unter CI versteht man die Praxis, Codeänderungen frühzeitig und häufig auf den main-Branch zu bringen. Dabei wird die Software automatisch getestet und und Codequalität geprüft. Dadurch können Fehler und Sicherheitsprobleme frühzeitig erkannt werden, sowie Merge-Konflikte vermieden werden

**Continuous Delivery/Deployment**
Für CD muss die CI im Projekt umgesetzt sein.
Continuous Delivery und Deployment werden oft Synonym verwendet. 

*Continuous Delivery* nimmt die Software aus der CI-Pipeline und führt weitere Automatisierte Tests durch (z.B. E2E-Tests). Anschließend wird sie dem Geschäftsteam zum Release geliefert.

*Continuous Deployment* geht einen Schritt weiter und stellt die neue Softwareversion automatisch auf den Test (und je nach System den Live) Umgebungen bereit.

---
# Ticketsysteme
Ein Ticketsystem ist eine Art von Software, um Empfang, Bestätigung, Klassifizierung und Bearbeitung von Kundenanfragen (Tickets bzw. Fälle) zu handhaben.

Eine Kundenanfrage wird also in ein Ticket geschrieben und kann nun Personen, Funktionen oder Abteilungen zugewiesen werden. Der Fortschritt kann nun z.B. auf einem Kanban-Board verfolgt werden.

---
# Open Source Software
Als *Open Source Software* wird jene Software bezeichnet, deren Quellcode öffentlich zugänglich und von jeder Person eingesehen, geändert und genutzt werden kann. Sie ist kostenlos.

**Vorteile:**
- Kostenersparnis
- Anpassbarkeit
- Sicherheitslücken werden schnell geschlossen
- kein Vendor-Lock-In

**Nachteile:**
- kein Professioneller Support
- Komplexität
- Fragmentierung

---
# Green IT
Green-IT zielt darauf ab, die Nutzung von IT über den gesamten Lebenszyklus hinweg Umweltschonend zu gestalten.

**Hardware Maßnahmen:**
- Energiesparende Hardware
- Umweltschonende Herstellung
- Recycling
- Nachhaltiges Design

**Software Maßnahmen:**
- ressourcensparende Programmierung und Prozesse
- Einsatz von IT zur Reduktion des Umwelteinflusses durch andere Bereiche (z.B. Heizen)