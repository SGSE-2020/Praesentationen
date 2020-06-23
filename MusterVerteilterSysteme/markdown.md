class: center, middle
# Muster verteilter Systeme
---

# Agenda
1. **Begrifflichkeiten**
    - Cloud Native
    - DevOps
    - Serverless
2. **Architekturen**
    - Schichtenarchitektur
    - Web-Queue-Worker
    - Event-Driven-Architektur
    - Big Data und Big Compute
    - Microservices (im Detail)
---

class: center, middle
# Begrifflichkeiten
---

class: middle
### Warum unsere Applikation in der Cloud nicht funktioniert

- Warum funktioniert unsere Applikation in der Cloud nicht?
- Warum haben wir so eine schlechte Performance?
- Warum ist unsere Anwendung nicht erreichbar?
- Warum haben wir ständig so viele Fehler?
---

# Cloud fremd
.image[![n-Tier](./images/monolith.png)]
---

class: middle
# Cloud Native
### "Wir sollten unsere Applikation für die Cloud entwickeln."

Wir erhalten Cloud Native Softwaresysteme durch:
- Cloud Softwarearchitekturen
- einen hohen Automatisierungsgrad
- die Bevorzugung von Cloudservices
---

class: middle
# DevOps
### "Wir sollten strikt mit unseren IT-Operations zusammenarbeiten."
DevOps bedeutet für uns:
- die Kooperation zwischen Entwicklern und IT-Operations
- Bereitstellung von Werkzeugen für die Entwicklung, Betrieb und Wartung
- andauernde Qualitätssicherung unserer Produkte
- einen hohen Automatisierungsgrad unseres Deployments
---

class: middle
# Serverless
### "Ermöglicht uns, unabhängig von IT-Operations zu arbeiten."
Serverless Server ermöglichen uns:
- den IT-Operations aufwand zu minimieren
- dem Serviceprovider die Serverbereitstellung zu überlassen
- Server dynamisch mit Ansprüchen des Gesamtsystems zu skalieren
- kosten zu senken. Wir bezahlen, was wir verbrauchen (Utility Computing)
---

class: center, middle
# Architekturen
## Muster verteilter Systeme 
---

# Schon wieder Schichtenarchitekturen
.image[![n-Tier](./images/3_tier.png)]
---

# Schichtenarchitektur? Verteilte Systeme? 
.image[![n-Tier](./images/2_tier_equal.png)]
---

## Schichtenarchitekturen können hochkomplex sein...
.image[![n-Tier](./images/5_tier.png)]
---

## ... aber auch super simpel
.image[![n-Tier](./images/1_tier.png)]
---

class: middle
# Tiere der Schichtenarchitektur
Grundsätzlich existieren 3 Standard-Architekturen:
- 1-Tier für Desktopanwendungen
- 2-Tier für Client-Server Anwendungen
- 3-Tier für einfache Web-Applikationen
---

# Die Schichtenarchitektur 
#### Einsatzbereiche
- Desktopanwendungen
- einfache Klient/Serveranwendungen
- einfache Webanwendungen

#### Vorteile
- geringer Lernaufwand
- einfache Entwicklung
- klare Einteilung grober logischer Zusammenhänge

#### Nachteile
- führt oft zu monolithischem Design
- nicht immer leicht skalierbar
- Datenintegrität lediglich beschränkt gewährleistet
- Aufbau und Struktur sind nicht definiert
---

# Web-Queue-Worker-Architektur
.image[![Web-Queue-Worker](./images/web-queue-worker.png)]
---

# Die Web-Queue-Worker-Architektur
#### Einsatzbereiche
- ressourcenintensive Vorgänge
- zeitintensive Vorgänge
- Vorgänge ohne direktes Feedback

#### Vorteile
- Zustandslosigkeit des Systems
- asynchrone Ausführung lang andauernder Aufgaben
- Starke Entkopplung durch Verwendung einer Warteschlange

#### Nachteile
- Frontend und Worker können sich monolithisch entwickeln
- Kein direktes Feedback zu Problemen von Aufgaben in der Warteschlange
- Geschäftslogik befindet sich zu großen Teilen innerhalb des Frontends
---

# Event-Driven-Architektur
.image[![Event-Driven-Architektur](./images/event_driven_architecture.png)]
---
class: middle
# Verfahren der Event-Driven-Architektur
Simple-Event-Processing
- Nachrichten lösen direkte Reaktionen aus

Complex-Event-Processing
- Nachrichten stehen in Abhängigkeit

Event-Stream-Processing
- Verknüpfung durch Streaming
---

# Die Event-Driven-Architektur
#### Einsatzbereiche
- Systeme welche sich Ereignisse teilen
- Systeme mit Echtzeitanforderungen
- Vorgänge ohne direktes Feedback

#### Vorteile
- Starke Entkopplung zwischen Produzenten/Konsumenten
- Einfaches Hinzufügen neuer Produzenten/Konsumenten
- Asynchrone Verarbeitung von Aufgaben
- Hoch skalierbar und verteilt
- Nachrichten werden garantiert bearbeitet

#### Nachteile
- Nachrichtenreihenfolge nicht sichergestellt
- Nachrichten müssen bei Erhalt validiert werden
- Bei Fehlern ist kein Standardverhalten definiert
- Netzwerkverzögerung bei verteilten Arbeiten
---

# Big Data und Big Compute
.image[![Big Compute](./images/big_compute.png)]
---

# Die Big Data und Big Compute-Architektur
#### Einsatzbereiche
- Berechnungen von Flüssigkeitsdynamiken für Schiffsschrauben
- Vorhersage von Geldflüssen in Bruchteilen für Börsentransaktionen
- Modellierungen für die geologische Ölexploration
- Wirkstoffentwicklung und Wirkstoffanalyse in der Pharmaindustrie
- Simulationen für die Entwicklung und Anwendung von Atomwaffen
- Bearbeitung von Daten, die für Rechensysteme zu groß sind

#### Vorteile
- Hohe Performance
- Skalierung mit der Aufgabenanforderung	
- Komplexe Probleme können zeitnah gelöst werden	

#### Nachteile
- Hoher Aufwand für die Hardwarebereitstellung
---

# Microservices
.image[![Sidecar](./images/microservice_database.png)]
---

# Microservices Datenbank alternative
.image[![Sidecar](./images/microservice_database_extern.png)]
### Herausforderungen
- Datenbank Lizenzmanagement
---

# Kommunikation
.image[![Sidecar](./images/messaging.png)]
---

# CQS und CQRS
#### Command-Query-Seperation
- Strikte Trennung von Objektmethoden in Queries und Commands
- Lässt sich ähnlich dem CRUD-Pattern in Vorgänge einteilen
  - nicht destruktiv: Queries
  - destruktiv: Commands

#### Command-Query-Responsibility-Segregation
- Die Einteilung durch CQS findet in verschiedenen Komponenten statt
---

# Event-Sourcing
.image[![Sidecar](./images/event_sourcing.png)]
---

# Wir müssen wachsen!
.image[![Sidecar](./images/microservice_replication.png)]
---

class: middle
# Warum wachsen wir?
- Die Anforderungen an unser System ändern sich
  - Erhöhte Auslastung: 1 mio. statt 10k Aufrufe pro Sekunde
  - Kosten Ersparnis: Kleine Nodes sind Günstiger
  - Wir haben internationale Kunden: fast delivery
- Unser System ändert sich
  - Wir wollen schneller verteilt arbeiten
---

# Scale Up!
.image[![Sidecar](./images/scaling_vertical.png)]
---

# Scale Out!
.image[![Sidecar](./images/scaling_horizontal.png)]
---

# Was machen wir da eigentlich?
.image[![Sidecar](./images/microservice_confusion.png)]
---

# Load-Balancing 1
### Last nach Dienst und Aufrufpfad verteilen
.image[![Sidecar](./images/load_balancer_dienst_query.png)]
---

# Load-Balancing 2
### Last nach Latenz und geostrategischer Kriterien
.image[![Sidecar](./images/load_balancer_geo.png)]
---

# Load-Balancing 3
### Last nach Auslastung individueller Services
.image[![Sidecar](./images/load_balancer_utilization.png)]
---

# Geht da noch mehr?
.image[![Sidecar](./images/load_balancer_dienst_query.png)]
---

# Na klar!
.image[![Sidecar](./images/api_gateway.png)]
---

# Wie sieht das denn im Detail aus?
.image[![Sidecar](./images/api_gateway_load_balancer.png)]
---

# Woher kennt unser API-Gateway die Routen?
.image[![Sidecar](./images/discovery_serverside.png)]
---

# Kann ein Klient das auch?
.image[![Sidecar](./images/discovery_clientside.png)]
---

class: middle
# Discovery-Methoden im Vergleich
###Client-Side-Discover
- Verschiebt die Zuständigkeit der Beschaffung von Routinginformationen zu individuellen Klienten

###Server-Side-Discover
- Kapselt die gesamte Geschäftslogik einer Microservice-Infrastruktur und hält diese geheim
---

# Fehlerbehandlung
.image[![Sidecar](./images/fehlerbehandlung.png)]
---

# Logging und Monitoring
.image[![Sidecar](./images/logging.png)]
---

# Transaktionen
.image[![Sidecar](./images/saga.png)]
---

# Die Microservicearchitektur
#### Einsatzbereiche
- Video- und Game-Streaming
- Komplexe Web-Shops und Web-Anwendungen
- Verteilte Anwendungen innerhalb des SmartCity-Softwareprojekts :-)

#### Vorteile
- Flexibilität durch unabhängige Bereitstellung	
- Isolation und Hoheit über Daten einzelner Services		
- System kann beliebig je nach Auslastung skaliert werden
- Fehler führen nicht zum Ausfall des Gesamtsystems			
- Codebasis einzelner Services ist besser überschaubar	

#### Nachteile
- Komplexes und großen Gesamtsystem
- Fehleranalyse kann eine Herausforderung sein
---

class: center, middle
# Das wars! 
#### Oder etwa nicht?
---

# Wir Entwickeln eine neue Applikation!
.image[![Sidecar](./images/sidecar_without.png)]
### Herausforderungen
- Individuelle Implementierungen fehleranfällig
- Neuentwicklungen von Standardkomponenten erforderlich
- Hoher Zeit und Ressourcenaufwand für Pflege und Wartung
---

# Outsourcing von Nebenläufigkeiten
.image[![Sidecar](./images/sidecar_with_proxy.png)]
---

# Das Sidecar-Pattern als verwaltete Proxy
.image[![Sidecar](./images/sidecar_management.png)]
---

class: center, middle
# Und wie verhält sich das alles in einer verteilten Umgebung? 
---

# Service-Mesh - Microservice ~~2.0~~ 1.1
.image[![Service-Mesh](./images/sidecar_service_mesh.png)]
---

# Service-Mesh - Topologie
.image[![Service-Mesh](./images/service_mesh_topologie.png)]
#### Zusammengefasst
 - Regelt Netzwerkverkehr und Zugriffe im Detail
 - Standardisiert Nebenläufigkeiten
---

# Vor- und Nachteile eines Service-Mesh
### Vorteile
- Inter-Service-Kommunikation ist durch SideCars(Proxys) standardisiert
- Metrik und Zustandserfassung ist durch SideCars(Proxys) standardisiert
- Nebenläufigkeiten wie Verschlüsselung werden automatisch umgesetzt
- Service Implementierung fokussieren sich auf Kernfunktionalitäten
- Services werden "schlanker" und kommen mit weniger Containern aus
- Nebenläufigkeiten können zentral gesteuert und verwaltet werden

### Nachteile
- Erhöhte Komplexität für die Erfassung des Gesamtbildes
- Fehlkonfigurationen können das Netzwerk destabilisieren
- Auslastung einer Anwendung wird nicht erfasst
---

class: center, middle
# Das wars! 
#### Danke für eure Aufmerksamkeit!
