# IHK Projektantrag - Fachinformatiker Systemintegration (V2)

**Thema:** Migration einer Server-Infrastruktur, Implementierung eines modernen Netzwerk- und Sicherheitssystems sowie Aufbau einer Automatisierungsplattform im Neubau unter Berücksichtigung kaufmännischer Aspekte.

---

## 1. Projektbeschreibung
Das Unternehmen bezieht einen neuen Standort (Neubau). Die vorhandene IT-Infrastruktur am alten Standort ist veraltet und bietet nicht die benötigte Performance sowie Sicherheitsfeatures für den neuen Betrieb.
Mein Auftrag umfasst die kaufmännische Planung, die technische Konzeption sowie die physische Umsetzung der neuen Netzwerkinfrastruktur. Ein wesentlicher Teil ist die Modernisierung der Serverlandschaft und die Einführung einer Automatisierungslösung.

**Kernaufgaben:**
*   **Kaufmännische Planung:** Durchführung eines Preisvergleichs und Angebotsvergleichs für die Hardware (Switch, Router, Server, Kameras). Erstellung einer Kosten-Nutzen-Analyse und ROI-Betrachtung.
*   **Netzwerkausstattung:** Installation einer UniFi-basierten Infrastruktur (Dream Machine SE, 24-Port PoE Switch, Access Points) im Neubau. Einrichtung eines segmentierten Netzwerks (VLANs für Management, Kameras, IoT, Produktion).
*   **Überwachungslösung:** Evaluation und Auswahl einer geeigneten Management-Software für die Reolink PoE-Kameras zur zentralen Videoüberwachung.
*   **Server-Modernisierung & Migration:** Inbetriebnahme des Lenovo ThinkSystem SE350 Edge-Servers. Migration bestehender kritischer Dienste (z. B. File-Server).
*   **Automatisierung:** Implementierung eines **n8n-Servers als Container** (z. B. via Docker) auf dem Lenovo Server zur Prozessautomatisierung.

---

## 2. Projektumfeld
Die Umsetzung erfolgt im Netzwerkschrank des Neubaus. Das Projekt umfasst die gesamte Kette vom Hardwareankauf über die physische Montage bis zur softwareseitigen Migration und Automatisierung.

---

## 3. Projektphasen mit Zeitplanung (Gesamt: 40 Stunden)

### 3.1 Planungsphase (10,5 h)
*   **Ist-Analyse & Soll-Konzept:** Aufnahme der Anforderungen und Standortbesichtigung (3 h)
*   **Hardware-Recherche & Angebotsvergleich:** Marktvergleich für kaufmännische Entscheidung (3 h)
*   **Wirtschaftlichkeitsbetrachtung:** ROI-Analyse und Budgetabstimmung mit dem Kunden (2 h)
*   **Risikoanalyse:** Identifikation von Migrations- und Ausfallrisiken sowie Minderungsstrategien (1,5 h)
*   **Technisches Design:** Erstellung des VLAN-Konzepts und Topologie-Plans (1 h)

### 3.2 Realisierungsphase (20,5 h)
*   **Vorkonfiguration:** Initial-Setup von Router, Switches und VLAN-Segmentierung (3,5 h)
*   **Software-Evaluation:** Vergleich und Auswahl der Surveillance-Software für die Kameras (2 h)
*   **Hardware-Einbau:** Physische Installation im Rack und CAT-Verkabelung am Patchpanel (3,5 h)
*   **Video- & WLAN-Setup:** Montage der Reolink-Kameras und Konfiguration der APs (3,5 h)
*   **Containerisierung & n8n:** Setup der Container-Laufzeitumgebung und Bereitstellung des n8n Containers (3,5 h)
*   **Migration:** Überführung der Bestandsdienste (z. B. lokale Datenbank/Files) auf das Neusystem (3,5 h)
*   **Kamera-Integration:** Anbindung der Kameras an die gewählte Management-Software (1 h)

### 3.3 Test- und Abnahmephase (4,5 h)
*   **Abnahmetests:** Systemprüfung (Durchsatz, Videoqualität, n8n-Workflows) (2,5 h)
*   **Übergabe & Einweisung:** Projektabnahme durch den Kunden und kurze Schulung (2 h)

### 3.4 Dokumentation (4,5 h)
*   **Kundendokumentation:** Erstellung von Übergabeunterlagen, Plänen und Wartungshinweisen (3,5 h)
*   **Wirtschaftlicher Projektabschluss:** Finale Kostenrechnung und Vergleich zum Angebot (1 h)

---

## 4. Dokumentation zur Projektarbeit
Es wird eine detaillierte Kundendokumentation erstellt, die das Pflichtenheft, Abnahmeprotokolle, Netzpläne und die Wirtschaftlichkeitsberechnung enthält.

---

## Bewertung (V2)

### Warum dieses Projekt überzeugt:
1.  **Hohe Komplexität:** Die Erweiterung um **n8n (Container-basiert)** und die **Software-Evaluation** hebt das Projekt deutlich über Standard-Installationen hinaus.
2.  **Transparente Wirtschaftlichkeit:** Der kaufmännische Teil ist durch den Angebotsvergleich und die ROI-Analyse stark gewichtet.
3.  **Saubere Planungsphase:** Die neu integrierte **Risikoanalyse** zeigt organisatorische Reife.

### Erfüllte Verbesserungsvorschläge (User & Agent):
*   **Max 3,5h Blöcke:** Alle Zeitblöcke wurden auf maximal 3,5 Stunden begrenzt.
*   **n8n Container:** Bereitstellung als Container auf dem Lenovo Server statt VM.
*   **VLAN Segmentierung:** Explizit im technischen Teil und in der Zeitplanung erwähnt.
*   **Software-Wahl:** Einplanung von Zeit für die Auswahl der Überwachungssoftware.
*   **Risikoanalyse:** Als fester Bestandteil der Planungsphase aufgenommen.
