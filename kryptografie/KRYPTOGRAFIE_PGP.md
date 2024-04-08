# KRYPTOGRAFIE PGP

## Aufgaben

### 1. Wie kann ich einen Public-Key verifizieren?

Dazu benötigt man den dazugehörigen Fingerabdruck, dieser ist der Hash des Publik-Keys und dient zur Überprüfung der Integrität des Keys.

### 2. Was versteht man unter Public Key Infrastruktur (PKI)?

Public Key Infrastruktur (PKI) ist ein System von Hardware, Software, Personen, Richtlinien und Verfahren, das zur Verwaltung von Public-Key-Zertifikaten und zur Absicherung der Kommunikation zwischen zwei Parteien verwendet wird.

### 3. Was bedeutet Certification-Authority (CA) und was Trust-Center (TC)?

Eine Certification Authority (CA) ist eine vertrauenswürdige Instanz, die digitale Zertifikate ausstellt und die Identität von Personen oder Organisationen überprüft. Ein Trust-Center (TC) ist ein sicherer Ort, an dem digitale Zertifikate und Schlüssel sicher aufbewahrt und verwaltet werden. Ein Trust-Center kann auch als Zertifizierungsstelle (CA) fungieren und digitale Zertifikate ausstellen.

### 4. Wer hat das Zertifikat für die Bankwebseite [www.ubs.com](https://www.ubs.com/) ausgestellt und wie lange ist es gültig?

DigiCert Inc
Gültig bis Freitag, 13. Dezember 2024 um 00:59:59

### 5. Wer hat das Zertifikat für die für die Schulwebseite [www.tbz.ch](https://tbz.ch/) ausgestellt und wie lange ist es gültig?

Let's Encrypt
Gültig bis Sonntag, 30. Juni 2024 um 19:35:24

### 6. Wer hat das Zertifikat für die für die Webseite [www.example.ch] ausgestellt und wie lange ist es gültig?

Haben kein Zertifikat.

### 7. Wählen sie irgendeine Applikation aus, die auf ihrem PC installiert ist. Stellen sie sich nun vor, sie müssten diese von Hand aktualisieren oder aus Kompatibilitätsgründen auf eine frühere Version zurückstufen. Wo finden sie aktuelle und frühere Versionen ihrer Software und wie wird sichergestellt, dass die dort angebotene SW-Version auch wirklich echt ist bzw. vom SW-Entwickler stammt?

Auf der offizielle Website der Software gibt es meistens eine Download Seite, wo die gewünschte Version heruntergeladen werden kann. Um dies zu prüfen gibt es meisten eine digitale Signatur.

### 8. Erstellen sie eine virtuelle Linux-Maschine mit z.B. VirtualBox und Ubuntu. Richten sie nun auf ihrem WIN-PC eine Remoteverbindung via ssh zu ihrem Linux-PC ein. Überprüfen sie die Verbindung. Wäre auch eine graphische Anbindung möglich?

Ja

### 10. Öffnen sie die beiden folgenden Webseiten und achten sie auf die Unterschiede in der Webadresszeile. Was stellen sie bezüglich Protokoll und Zertifikat fest?

- [https://juergarnold.ch](https://juergarnold.ch)
- [https://www.zkb.ch](https://www.zkb.ch)

Es werden andere Zertifikate verwendet.

### 11. Wenn sie sich mit Zertifikaten befassen, fallen ihnen früher oder später folgende Anbieter bzw. Webseiten auf

- [http://www.cacert.org](http://www.cacert.org/)
- [https://letsencrypt.org/de](https://letsencrypt.org/de)

#### Was genau wird hier zu welchen Konditionen angeboten?

CAcert bietet kostenlose Zertifikate an, während Let's Encrypt kostenlose Domain-Validated-Zertifikate anbietet. Let's Encrypt-Zertifikate sind automatisiert und haben eine begrenzte Gültigkeitsdauer.

### 12. Folgende TLS Zertifikatsarten werden unterschieden: Domain Validated, Organization Validated und Extended Validation. Sie möchten einen Webshop betreiben, wo mit Kreditkarte bezahlt werden kann. Welcher Zertifikatstyp ist der richtige?

Für einen Webshop, wo mit Kreditkarten bezahlt wird, ist ein Extended Validation (EV) Zertifikat der richtige Typ, da es die höchste Validierungsebene bietet und das höchste Maß an Sicherheit und Vertrauen für Kunden bietet.

### 13. Studieren sie den Beitrag auf der Webseite Let's Encrypt "Wie es funktioniert"

[https://letsencrypt.org/de/how-it-works/](https://letsencrypt.org/de/how-it-works/)

#### Was ist der Unterschied zwischen OpenPGP und X.509?

OpenPGP und X.509 sind verschiedene Standards für die Verschlüsselung und Authentifizierung. OpenPGP ist ein Verschlüsselungsstandard für E-Mails, während X.509 ein Standard für die Zertifikatshierarchie und Authentifizierung im Web ist.

### 14. Erklären sie den Aufruf einer sicheren Webseite. (HTTPS) Wie ist der Ablauf beim Protokoll TLS? Wo genau kommen die Zertifikate ins Spiel?

Beim Aufruf einer sicheren Webseite (HTTPS) wird eine verschlüsselte Verbindung zwischen dem Client und dem Server hergestellt. Der Ablauf beim TLS-Protokoll beinhaltet Handshake, Authentifizierung, Schlüsselaustausch und verschlüsselte Datenübertragung. Zertifikate kommen ins Spiel, um die Identität des Servers zu authentifizieren und die Verschlüsselungsschlüssel zu übermitteln.

### 15. Was bedeutet S/MIME?

S/MIME steht für Secure/Multipurpose Internet Mail Extensions und ist ein Standard zur sicheren Übertragung von E-Mails mittels Kryptographie.

### 16. Aus gesetzlichen Gründen sind sie verpflichtet, den gesamten geschäftlichen EMailVerkehr zu archivieren, auch den verschlüsselten. Was ist das Problem dabei und wie könnte man dies lösen?

Das Problem beim Archivieren verschlüsselter geschäftlicher E-Mails besteht darin, dass der Inhalt der E-Mails nicht ohne den entsprechenden privaten Schlüssel entschlüsselt werden kann. Eine mögliche Lösung wäre die Archivierung von E-Mails vor der Verschlüsselung oder das Management der privaten Schlüssel zusammen mit den verschlüsselten E-Mails.
