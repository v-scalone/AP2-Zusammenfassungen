

# **WhiteBox Testing**

# **BlackBox Testing**

# **Last- & Performancetest**

# **E2E - Integration - Unit (siehe Bild)**

![bild](Bilder\IMG_20250415_144539_069.png)

Im E2E Test wird nichts gemockt!
Heißt es gibt zwei Welten, da im Unit-Test durchaus viele Zustände gemockt werden können. Somit kann ein Zustand entstehen im Unit-Test der nur da testbar ist! Um die Qualität der Software zu gewährleisten muss daher auf die Test-Pyramide geachtet werden. Genug Unit-Tests und gezielte E2E-Tests.
E2E-Tests sind aufwändiger zu gestalten und auch teurer, weil für einen E2E-Test die gesamte Anwendungslogik laufen muss. Vom Frontend, über das Backend bis hin zum Datenbankserver z.B.. Erst wenn alle erforderlichen Komponenten für die Anwendung laufen kann ein E2E-Test stattfinden.

Beispiel:
In einer Anwendung existieren Nutzer. Ein Nutzer war 2 Jahre lang inaktiv. Die Anwendungslogik besagt das inaktive Nutzer die sich wieder einloggen zuerst eine Email zum Authentifizieren bekommen.
Diese Logik ist in einem E2E-Test sehr schwer abzutesten, da ein E2E-Test keine Einsicht in die "inaktiv"-Logik hat.
Ein Unit-Test hingegen kann einen Testnutzer erstellen, das Datum der Erstellung auf vor 2 Jahre mocken und darauf dann einen Unittest durchführen.
In diesem Beispiel ist eine "inaktiv"-Logik nur wirklich von einem Unittest abzutesten. Ein E2E-Test könnte nur abtesten ob eine Authentifizierung-Email verschickt oder angekommen ist.


