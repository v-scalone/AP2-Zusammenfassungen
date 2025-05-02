# IT-Grundschutz
**Schutzziele:**
- *Vertraulichkeit* – Schutz vor unbefugtem Zugriff
- *Integrität* – Schutz vor Manipulation und Datenverfälschung
- *Verfügbarkeit* – Sicherstellung der System- und Datenverfügbarkeit
- *Authentizität* – Sicherstellung der Echtheit von Daten und Identitäten
- *Verbindlichkeit* – Nachweisbarkeit von Aktionen und Transaktionen

---
# Schutzmaßnahmen
**Passwörter:** 
Starke und einzigartige Passwörter sowie Zwei-Faktor-Authentifizierung schützen Konten effektiv.

**Firewalls:** 
Firewalls blockieren unautorisierte Zugriffe und sollten regelmäßig aktualisiert und überwacht werden.

**Backups:**
Regelmäßige und sichere Backups bewahren Datenverlust vor und müssen getestet werden.

**Verschlüsselung:**
Verschlüsselung schützt Daten bei Speicherung und Übertragung vor unbefugtem Zugriff.

---
# Authentifizierung vs Autorisierung
Bei der **Authentifizierung** handelt es sich um den Prozess der Überprüfung der Identität, während bei der **Autorisierung** festgelegt wird, was erlaubt ist, sobald die Identität bestätigt ist – d.h. die Berechtigungen.

---
# TLS/SSL
**Definition:** TLS (Transport Layer Security) ist ein Protokoll zur Verschlüsselung von Datenverkehr. TLS ist der direkte Nachfolger von SSL, welches veraltet ist.

Der Server Besitzt ein SSL-Zertifikat, ausgestellt von einer anerkannten Zertifikatsstelle (certificate authority). Dieses enthält unter anderem den public key des Servers.

Bei der Verbindungsherstellung übergibt der Server das Zertifikat und ein “server random” an den Client, dieser Überprüft dieses und sendet anschließend ein verschlüsseltes “premaster secret” an den server.

Aus dem “client random”, dem “server random” und dem “premaster secret” den Sitzungsschlüssel, welcher für die symmetrische Verschlüsselung verwendet wird.
![[ap2-TLS-Handshake.png]]

**Aus der Prüfung 2022:**
TLS (Transport Layer Security) arbeitet nach dem Prinzip der **hybriden Verschlüsselung**. Dabei werden im Rahmen des TLS-**Handshakes** zunächst die **Public-Keys** ausgetauscht, um die weitere Kommunikation **asymmetrisch** zu verschlüsseln. Nachdem sich Client und Server auf einen Shared-Key geeinigt haben, wird die weitere Verbindung symmetrisch verschlüsselt. Die hybride Verschlüsselung wird verwendet, da das asymmetrische Verfahren sehr rechenaufwendig ist und man somit die Vorteile aus beiden Verfahren (symmetrisch und asymmetrisch) kombinieren kann.
[AWS Artikel](https://aws.amazon.com/de/compare/the-difference-between-ssl-and-tls/)
[digicert Artikel, auch HTTPS](https://www.digicert.com/de/what-is-ssl-tls-and-https)

---
# OAuth2 - Autorisierung
**Flow:**
1. *Client* fragt beim *Autorisierungsserver* mit Client-ID und Client-Secret zugriff an.
2. Der *Autorisierungsserver* authentifiziert den Client.
3. 
4. Der *Autorisierungsserver* und der *Ressourcenbesitzer* kommunizieren, um den Zugriff zu erteilen.
5. Zugriffstoken wird an den *Client* übergeben.
6. Mit dem Zugriffstoken kann der *Client* die Ressource beim *Ressourcenserver* Anfragen
![[ap2-oauth2.png]]

---
# SSO (Single Sign-on)
**Übersicht:** Statt sich bei jedem Dienst einzeln anmelden zu müssen, kann man sich bei einem zentralen Identity Provider (IDP) Anmelden

**Vorteile:** 
- Passwörter nur beim IDP
- IT-Sicherheit kann auf den IDP Fokussiert werden
- erschwert Phishing-Attacken
- bessere Übersicht über erteilte Rechte
- Sicherheitsvorfälle leichter zu adressieren an Zentraler stelle
**Nachteile:**
- Verfügbarkeit aller Systeme hängt nun vom IDP ab
- Ein Zugang → Zugriff auf viele Systeme

**Umsetzung:**
Meist mit OAuth2 oder SAML Tokens die dem Client ausgestellt werden. 
Ein lokaler Passwort-Manager mit auto-fill zählt technisch gesehen auch als SSO-System.

---
# Verschlüsselung
#### Symmetrisch vs Asymmetrisch
**Symmetrisch:** Ein Schlüssel wird zum ver- und entschlüsseln Verwendet. Weniger rechenaufwendig und schneller. Dafür müssen aber beide Seiten den Schlüssel kennen.

**Asymmetrisch:** Es gibt ein Schlüsselpaar. Von einem Schlüssel verschlüsselt können die Daten nur vom anderen entschlüsselt werden und andersrum. Public-Private Keys. Teurer aber kein Problem den public key über das Internet zu versenden.

**Hybrid:** Asymmetrisches  Verfahren wird Verwendet, um sich über den symmetrischen Schlüssel auszutauschen. Das beste aus beiden Welten, Sicherheit und Geschwindigkeit. z.B. [[IT-Sicherheit#TLS/SSL"|TLS/SSL]]

#### Bitlocker
Festplattenverschlüsselung von Windows, das Sektorenweise mit [AES](https://de.wikipedia.org/wiki/Advanced_Encryption_Standard) Verschlüsselt.

---
# Zugriffskontrolle im Netzwerk
**RADIUS** - Remote Authentication Dial-In User Service
RADIUS (Remote Authentication Dial-In User Service) ist ein Netzwerkprotokoll, das zur Authentifizierung, Autorisierung und zur Buchhaltung (Accounting) von Benutzern verwendet wird, die auf ein Netzwerk zugreifen möchten. 
- Zentraler Authentifizierungsserver
- *Funktionsweise*:
    - *Anfrage*: Ein Netzwerkgerät (NAS - Network Access Server) sendet eine Zugriffsanfrage an den RADIUS-Server.
    - *Authentifizierung*: Der RADIUS-Server überprüft die Anmeldeinformationen des Benutzers.
    - *Autorisierung*: Wenn die Authentifizierung erfolgreich ist, autorisiert der RADIUS-Server den Zugriff basierend auf den Benutzerrechten.
    - *Accounting*: Der RADIUS-Server protokolliert die Sitzungsdaten für spätere Analyse und Abrechnung.

**Kerberos**
Kerberos ist ein weiterer zentraler Dienst für die Zugriffskontrolle. Es arbeitet mit Tickets und funktioniert als SSO-System.
- *Funktionsweise*:
    - *Authentifizierung*: Der Benutzer sendet eine Anfrage an den Authentifizierungsserver (AS) im KDC.
    - *Ticket-Granting Ticket (TGT):* Der AS sendet ein TGT zurück, das der Benutzer verwenden kann, um weitere Tickets für den Zugriff auf verschiedene Dienste zu erhalten.
    - *Service Ticket*: Der Benutzer sendet das TGT an den Ticket-Granting Server (TGS) im KDC, um ein Service Ticket für einen bestimmten Dienst zu erhalten.
    - *Zugriff*: Mit dem Service Ticket kann der Benutzer auf den gewünschten Dienst zugreifen.