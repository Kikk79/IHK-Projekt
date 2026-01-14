# Projektdokumentation (ANONYMISIERT)

**Thema:** Aufbau eines zentral verwalteten, physischen Zugangssteuerungssystems für Serverschränke in Fremdrechenzentren

**Prüfling:** Max Mustermann
**IHK:** [IHK-REGION]
**Prüflingsnummern:** AP1 - [ID1] / AP2 - [ID2]

**Ausbildungsbetrieb:** Muster Seminare GmbH
[STRASSE]
[PLZ] [ORT]

**Praktikumsbetrieb:** [FIRMA] Data Processing GmbH
[STRASSE-P]
[PLZ-P] [ORT-P]

---

## Inhalt
1. Einleitung
2. Projektplanung
3. Projektrealisierung
4. Funktionstest
5. Fazit
6. Glossar

---

## 1. Einleitung
Diese Dokumentation wurde im Rahmen der betrieblichen Projektarbeit zur Umschulung zum Fachinformatiker für Systemintegration erstellt.

### 1.1 Das Unternehmen
Die [FIRMA] IT Services GmbH ist ein mittelgroßes, global tätiges Unternehmen mit Hauptsitz in [STADT], welches im Tourismussektor tätig ist und ihren Kunden, zu denen u. a. große Reisebetreiber und Fluglinien gehören, die benötigte Infrastruktur hinsichtlich Reisebuchung und Finanzabwicklung zur Verfügung stellt.

### 1.2 Projektumfeld
Als Praktikant in der Abteilung Data Center Management war ich hauptsächlich für die Verwaltung des lokalen Rechenzentrums, sowie der im Rahmen der Cloudmigration neu aufgebauten, sog. PoPs (Points of Presence) in verschiedenen externen Rechenzentren zuständig.

### 1.3 Betriebliche Schnittstellen
An der Durchführung waren neben mir selbst noch beteiligt:
- [PERSON-A] (Direkter Vorgesetzter, Teamleiter DCM) für die initiale Beauftragung und Vorgaben über die zu nutzenden Systeme/Hardware
- [PERSON-B] (Kollege, Teammitglied DCM) für die Bereitstellung der nötigen internen Zugänge verantwortlich.

### 1.4 Motivation und Zielsetzung
Durch die cloudbasierte Neuausrichtung des Unternehmens und die damit verbundene Installation/Konfiguration von Hardware durch verschiedene Techniker in diversen Fremdrechenzentren und die durch Zugangsprobleme entstehenden Kosten und Verzögerungen, entstand das Anforderung, den physischen Zugang zu diesen Serverschränken ferngesteuert und zentral verwalten zu können.

Da mein Kollege, der mir die benötigten Zugänge und Rechte auf den Servern zur Verfügung stellen sollte, unerwartet krankheitsbedingt über einen längeren Zeitraum ausgefallen ist und meine Arbeit wegen CoviD-19 Vorschriften größtenteils von zu Hause aus zu erledigen war, wurde ich damit beauftragt ein Proof of Concept für die Bereitstellung des Zugangssteuerungssystems anzufertigen, und wenn möglich zu einem späteren Zeitpunkt umzusetzen.

---

## 2. Projektplanung

### 2.1 IST-Analyse
Aufgrund der stetig steigenden Aktivitäten durch den Umzug in die Cloud und die dadurch benötigten PoPs in immer mehr Rechenzentren, steigt auch der Bedarf an Technikerbesuchen um z.B. gelieferte Hardware zu installieren oder Änderungen an bestehenden Konfigurationen der Serverschränke vorzunehmen. Da es sich bei den Rechenzentren um viele verschiedene Betreiber handelt, hat natürlich auch jeder Betreiber seine eigenen Systeme, wenn es darum geht Technikern den Zugang zu den Serverschränken zu verschaffen. Leider mussten wir feststellen, dass außerordentlich viele Techniker mangels Zugangsberechtigung ihre Termine nicht wahrnehmen konnten und dadurch u.a. wichtige Meilensteine verzögert und zusätzliche Kosten verursacht wurden.

### 2.2 SOLL-Analyse
Von der Teamleitung wird nach Rücksprache mit allen Teammitgliedern eine zentrale Lösung angestrebt, welche das Öffnen der Serverschränke aus der Ferne ermöglicht. Im Zuge dessen sollen an allen Serverschränken ferngesteuerte smarte Schlösser angebracht werden, welche so konfiguriert werden, dass das Team zentral die Zugänge durch dynamische Vergabe von PIN Nummern und die direkte Kommunikation an die Techniker verwalten kann, um Verzögerungen und Mehrkosten in Zukunft vermeiden zu können. Aufgrund bereits bestehender Geschäftsbeziehungen wurde der Hersteller des Schließsystems von der Teamleitung ausgewählt. Aufgrund der Umstände besteht meine Aufgabe darin, eine virtuelle Umgebung nachzubauen, die den Gegebenheiten der Firma soweit wie möglich entspricht und mit Hilfe eines zu besorgenden Testgerätes einen Proof of Concept zu erstellen.

### 2.3 Aufbau des Testsystems

#### 2.3.1 Hostsystem
Aufgrund fraglicher Performance des Firmenlaptops wird hier mein Privat-PC im Homeoffice mit folgenden Leistungsdaten genutzt:
- CPU: Intel 8-Kern CPU
- RAM: 32 GB (4x8) 3200Mhz
- Speicher: SSD mit 512 GB exklusiv für virtuelle Gastsysteme
- OS: Windows 11 (mit WSL)

Als Router kommt eine [ROUTER-MODELL] zum Einsatz, an welche das geliehene Testschloss per Netzwerkkabel angeschlossen und mithilfe eine USB-C Kabels mit Strom versorgt wird.

#### 2.3.2 Auswahl der Virtualisierungsumgebung
Die Zielumgebung wurde durch eine Virtualisierung realisiert. Bei der Auswahl der Virtualisierungsumgebung beschränke ich mich auf die 3 größten Hersteller VMware, Oracle und Microsoft. Zum einen aufgrund meiner persönlichen Erfahrung und zum andere, da für die bei möglichen Problemen etliche nützliche Ressourcen und Informationen zur Verfügung stehen. Alle 3 erfüllen die nötigen Anforderungen zur Installation eines Windows Server 2019, aber nur Oracle und Microsoft sind frei erhältlich; daher habe ich mich für Virtualbox von Oracle entschieden.

### 2.4 Beschaffung der notwendigen Hard- und Software
Nach Besprechung mit der Teamleitung wurde mir ein Kontakt zum ausgewählten Dienstleister zur Verfügung gestellt, mit der Anweisung, mich um die Bereitstellung der benötigten Hard- und Software zu kümmern. Nach initialem Kontakt konnte ich den Dienstleister, den Anbieter des Schlosssystems, überzeugen, mir ein Testgerät, nämlich ein Schloss, und die benötigte Serversoftware sowie evtl. benötigter Anleitungen zur Verfügung zu stellen. Das Equipment sowie ein Link für den Download der nötigen Software auf Github wurden nach einigen Wochen zu mir ins Home-Office geschickt.

---

## 3. Projektrealisierung

### 3.1 Installation der Virtualisierungsumgebung
#### 3.1.1 Probleme mit Virtualbox
Nach Installation von Virtualbox 6.1.34 und der initialen Konfiguration der virtuellen Maschine erhalte ich Fehlermeldungen bezüglich Hyper-V. Nach längerer Recherche in einschlägigen Foren ließ sich herausfinden, dass Virtualbox noch Probleme mit aktiviertem Hyper-V hat und sich deshalb die Netzwerkverbindung nicht richtig konfigurieren lässt. Da das Hostsystem auf Windows 11 mit aktiviertem WSL läuft und produktiv genutzt wird, besteht keine Möglichkeit, Hyper-V auszuschalten. Ich habe mich für die sicherere Variante entschieden und die Virtualisierungsumgebung gewechselt.

#### 3.1.2 Umstieg auf Hyper-V
Nach Installation aller benötigten Hyper-V Komponenten steht als nächstes die Installation des Windows Server 2019 an.

### 3.2 Installation des Gast Betriebssystems (Windows Server 2019)
Die einzelnen Schritte der Installation von Windows Server 2019 wurden dokumentiert.

### 3.3 Installation / Konfiguration der Serversoftware
Die Serversoftware besteht aus 2 Paketen (Funktionsserver und Weboberfläche für die Verwaltung). Hierbei wird die Applikation als Service hinzugefügt und eine entsprechende Regel für die benötigten TCP Ports 4343 & 4344 in der windowseigenen Firewall erstellt.

### 3.4 Konfiguration des Schlosses
Da das Schloss mit voreingestellter IP und Netzmaske versandt wurde, musste ich mein Heimnetz umstellen.

### 3.5 Integration des Schlosses im Verwaltungsserver
Dank der im Schloss bereits erledigten Konfiguration taucht das Schloss auch automatisch unter dem Punkt NEW Locks auf.

---

## 4. Funktionstest
- Erster Funktionstest: Schloss mit PIN öffnen -> funktioniert
- Zweiter Funktionstest: Überprüfung der Rückmeldung in Verwaltungssoftware -> funktioniert
- Dritter Funktionstest: Steuerung des Schlosses über die Verwaltungssoftware -> fehlgeschlagen

Mögliche Ursachen wurden mit Hilfe des He
