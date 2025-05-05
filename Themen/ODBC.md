*ODBC (Open Database Connectivity)* ist eine standardisierte Schnittstelle, mit der Anwendungen auf verschiedene Datenbanksysteme zugreifen können – unabhängig vom Hersteller.

**Vorteile:**
- *Datenbankunabhängigkeit*: Eine Anwendung kann mit verschiedenen Datenbanken kommunizieren, solange ein passender ODBC-Treiber vorhanden ist.
- *Weit verbreitet*: Unterstützt viele Datenbanken (z. B. MySQL, SQL Server, Oracle).
- *Standardisiert*: Einheitliches API vereinfacht die Entwicklung.
**Nachteile:**
- *Performance*: Etwas langsamer als native Treiber, da es eine zusätzliche Abstraktionsschicht gibt.
- *Komplexe Einrichtung*: ODBC-Treiber müssen separat installiert und konfiguriert werden.
- *Plattformabhängigkeit*: Unterschiede bei der Treiberverfügbarkeit je nach Betriebssystem.