# IHK-Projektantrag

**Thema:** Migration einer Server-Infrastruktur, Implementierung eines modernen Netzwerk- und Sicherheitssystems sowie Aufbau einer Container-basierten Automatisierungsplattform im Neubau unter Berücksichtigung kaufmännischer Aspekte.

---

## 1. Projektbeschreibung (Problemstellung & Lösung)

Das Unternehmen bezieht einen neuen Standort (Neubau). Die vorhandene IT-Infrastruktur am alten Standort ist veraltet und bietet nicht die benötigte Performance sowie Sicherheitsfeatures für den neuen Betrieb. Mein Auftrag umfasst die kaufmännische Planung, die technische Konzeption sowie die physische Umsetzung der neuen Netzwerkinfrastruktur.

**Kernaufgaben:**

* **Kaufmännische Planung:** Durchführung eines strukturierten Preis- und Angebotsvergleichs für alle Hardware-Komponenten (Ubiquiti, Lenovo, Reolink). Erstellung einer Kosten-Nutzen-Analyse zur Budgetabstimmung mit der Geschäftsführung.
* **Netzwerkausstattung:** Installation einer UniFi-basierten Infrastruktur (Dream Machine SE, 24-Port PoE Switch, Access Points) im Neubau. Einrichtung eines segmentierten Netzwerks mittels VLANs (Management, Video, IoT, Produktion).
* **Überwachungslösung:** Evaluation, Auswahl und Implementierung einer geeigneten Management-Software für die Reolink PoE-Kameras zur zentralen Videoüberwachung.
* **Server-Modernisierung & Migration:** Inbetriebnahme des Lenovo ThinkSystem SE350 Edge-Servers. Migration bestehender kritischer Dienste vom Altsystem auf die neue Hardware.
* **Automatisierung:** Implementierung eines n8n-Servers als Container (z.B. mittels Docker) auf dem Lenovo Server zur Automatisierung betrieblicher Prozesse.

---

## 2. Projektumfeld

Die Umsetzung erfolgt direkt vor Ort im Neubau des Unternehmens (Rack-Installation). Die Migration und Konfiguration erfolgen unter Berücksichtigung maximaler Systemverfügbarkeit.

---

## 3. Projektphasen mit Zeitplanung (Gesamt: 40 Stunden)

### 3.1 Planungsphase (10,5 h)

* **Ist-Analyse & Soll-Konzept:** Aufnahme der Anforderungen und Standortbesichtigung (3 h)
* **Kaufmännische Analyse:** Hardware-Recherche, Angebotsvergleich und Wirtschaftlichkeitsberechnung (3,5 h)
* **Risikoanalyse:** Identifikation von Projektrisiken (z.B. Migrationsfehler) und Erarbeitung von Ausfallkonzepten (2,5 h)
* **Technisches Design:** Erstellung des VLAN-Konzepts und des Netzwerk-Topologieplans (1,5 h)

### 3.2 Realisierungsphase (20,5 h)

* **Netzwerk-Infrastruktur:** Vorkonfiguration von Router und Switches sowie Einrichtung der VLAN-Segmente (3,5 h)
* **Hardware-Installation:** Physischer Einbau im Rack und CAT-Verkabelung am Patchpanel (3,5 h)
* **Video- & WLAN-Setup:** Montage der Reolink-Kameras und Konfiguration der Access Points (3,5 h)
* **Software-Evaluation:** Vergleich und Auswahl der optimalen Surveillance-Software (2,5 h)
* **Server & Container:** Setup der Container-Runtime und Bereitstellung des n8n-Containers (3,5 h)
* **Anbindung n8n an extene Dienste:** Erstellung einer Dyndns Domain mit Let`s encrypt Certificat hinter einem nginx Server(2 h)
* **Migration:** Überführung der Bestandsdienste und Daten auf das neue Edge-System (3,5 h)
* **Integration:** Anbindung der Kameras an die gewählte Management-Software (0,5 h)

### 3.3 Test- und Abnahmephase (4,5 h)

* **Abnahmetest:** Prüfung der Funktionalität (Netzwerk-Durchsatz, Video-Feed, n8n-Workflows) (2,5 h)
* **Übergabe:** Projektabnahme durch den Kunden und Einweisung in die neuen Systeme (2 h)

### 3.4 Dokumentation (4,5 h)

* **Kundendokumentation:** Erstellung von Übergabeunterlagen, Netzwerkplänen und Wartungshinweisen (3,5 h)
* **Wirtschaftlicher Abschluss:** Finale Kostengegenüberstellung zum Angebot (1 h)

---

## 4. Dokumentation zur Projektarbeit

Es wird eine praxisorientierte Kundendokumentation erstellt, die das Pflichtenheft, Abnahmeprotokolle, Netzpläne und die tabellarische Hardware-Kalkulation enthält.

---

## Bewertung (Abschlussfazit)

Dieses Projekt ist für die Abschlussprüfung **hervorragend geeignet**, da es:

* Die geforderten **kaufmännischen Aspekte** (Angebotsvergleich, ROI) tiefgehend behandelt.
* Moderne Technologien (**Containerisierung/n8n**) nutzt, was die technische Tiefe unterstreicht.
* Durch die **VLAN-Segmentierung** Sicherheitsbewusstsein beweist.
* Alle Phasen der **vollständigen Handlung** (Planen, Durchführen, Kontrollieren) abdeckt.
