# VM vs VDI

## **Jede VDI ist eine VM, aber nicht jede VM ist eine VDI!**


---

## **Virtualisierung am Beispiel Server-Virtualisieren**

**Einfache Erklärung:**  
Server-Virtualisierung bedeutet, dass auf einem physischen Server (also ein echter, „anfassbarer“ Computer) mehrere „virtuelle“ Server gleichzeitig betrieben werden. Diese virtuellen Server verhalten sich wie eigenständige Computer, **teilen sich aber die Ressourcen** (Prozessor, Arbeitsspeicher, Festplatte) des einen echten Servers.

**Ausführliche Erklärung:**  
Bei der Server-Virtualisierung wird durch eine spezielle Software, den sogenannten **Hypervisor**, eine Abstraktionsschicht geschaffen. Diese Schicht trennt die Hardware des physischen Servers von den darauf laufenden Betriebssystemen. Statt dass nur ein Betriebssystem auf dem Server läuft, können durch Virtualisierung mehrere unabhängige „virtuelle Maschinen“ (VMs) gleichzeitig laufen – jede mit eigenem Betriebssystem und eigenen Anwendungen.

### Hauptvorteile der Server-Virtualisierung

- **Bessere Ressourcenauslastung:** Ein physischer Server wird effektiver genutzt, weil viele VMs parallel laufen.
- **Flexibilität:** Virtuelle Server können einfach erstellt, gelöscht, kopiert oder verschoben werden.
- **Kosteneinsparungen:** Weniger Hardware wird benötigt, was Strom, Platz und Wartung spart.
- **Isolation:** Fehler oder Probleme einer VM beeinflussen die anderen nicht direkt.


---

## **Unterschied VMs zu VDIs**

Einfache Erklärung:  
Eine **VM** (virtuelle Maschine) ist ein kompletter, unabhängiger „virtueller Computer“ auf einem Server.  
Ein **VDI** (Virtual Desktop Infrastructure) ist eine spezielle Art von VM, die als **persönlicher Desktop-Arbeitsplatz** für Benutzer dient und meist zentral im Rechenzentrum bereitgestellt wird.

|Merkmal|Virtuelle Maschine (VM)|Virtual Desktop Infrastructure (VDI)|
|---|---|---|
|**Definition**|Ein softwarebasiertes, eigenständiges Computer-System|Bereitstellung von Desktop-Umgebungen als VM|
|**Zweck**|Kann alles sein: Server, Entwicklungsumgebung etc.|Speziell für Benutzer-Desktops|
|**Nutzer**|Häufig IT-Admins, Applikationen|Endnutzer (z. B. Büroangestellte)|
|**Zugriff**|Meist per SSH, RDP oder Konsole|Per Remotedesktop, manchmal über Web-Browser|
|**Management**|Einzelne VMs manuell oder automatisiert verwalten|VDI-Lösung verwaltet Pools von Desktop-VMs|
|**Personalisierung**|Jede VM unabhängig konfigurierbar|VDIs können persistent (benutzerspezifisch) oder non-persistent (zurückgesetzt) sein|
|**Typische Nutzung**|Server-Betrieb, Testumgebungen, Netzwerkdienste|Homeoffice, Thin Clients, mobile Arbeit|


