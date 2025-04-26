# IT-Grundschutz
**Schutzziele:**



---
# TLS/SSL
**Definition:** TLS (Transport Layer Security) ist ein Protokoll zur Verschlüsselung von Datenverkehr. TLS ist der direkte Nachfolger von SSL, welches veraltet ist.

Der Server Besitzt ein SSL-Zertifikat, ausgestellt von einer anerkannten Zertifikatsstelle (certificate authority). Dieses enthält unter anderem den public key des Servers.

Bei der Verbindungsherstellung übergibt der Server das Zertifikat und ein “server random” an den Client, dieser Überprüft dieses und sendet anschließend ein verschlüsseltes “premaster secret” an den server.

Aus dem “client random”, dem “server random” und dem “premaster secret” den Sitzungsschlüssel, welcher für die symmetrische Verschlüsselung verwendet wird.
![[ap2-TLS-Handshake.png]]

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
**Nachteile:**
- Verfügbarkeit aller Systeme hängt nun vom IDP ab

**Umsetzung:**
Meist mit OAuth2 oder SAML Tokens die dem Client ausgestellt werden. 
Ein lokaler Passwort-Manager mit auto-fill zählt technisch gesehen auch als SSO-System.