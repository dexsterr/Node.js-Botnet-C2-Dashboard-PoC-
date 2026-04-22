# Distributed Agent Management System (C2 Architecture) 
*Proof of Concept / Case Study*

A comprehensive Command & Control (C2) dashboard built in Node.js for managing distributed automated agents. Features real-time telemetry, advanced anti-bot bypass mechanisms, and dynamic SOCKS5 proxy routing.

*(Note: Due to OPSEC and the sensitive nature of the bypass logic and proxy routing mechanisms involved, the full source code is kept private. This repository serves as a technical case study.)*

---

### Distributed Agent Management System (EN)

A practical Command & Control dashboard with a web interface, built using Node.js and Socket.IO.
The application automates the deployment of agents in remote environments, manages network routing to prevent detection, and provides real-time monitoring of all instances.

#### How does it work?

**Agent Management & Automation**
* Dynamically spawns and manages dozens of automated instances (bots) from a centralized web panel.
* Implements complex state machines to handle server-side challenges and bypass anti-bot verification without human intervention.
* Automates routine tasks and actions within the target environment.

**Network Routing (OPSEC)**
* Integrates dynamic SOCKS5 proxy routing to mask the origin IP of each agent.
* Prevents IP blacklisting and mimics legitimate distributed traffic.

**Fault Tolerance & Monitoring**
* Features a custom "watchdog" mechanism that monitors agent health.
* Automatically terminates unresponsive "zombie" processes and triggers reconnection procedures upon unexpected disconnects.

**C2 Dashboard & Telemetry**
* Real-time bidirectional communication using WebSockets (`socket.io`).
* Displays live system logs, agent connection status, and proxy health metrics.
* Allows mass execution of commands or granular control over individual agents.

**Alerting**
* Integrated with Discord API to send real-time alerts for critical events (e.g., proxy failures, server restarts, agent deaths).

#### Tech Stack
* Node.js, Express
* Socket.IO (Real-time WebSockets)
* Discord.js (Alerting)
* SOCKS5 Proxy Management

#### Security recommendations
* This architecture demonstrates techniques heavily used in Red Teaming and advanced automation.
* The methodologies discussed should only be applied to environments you explicitly own or have authorization to test.

*This project demonstrates practical skills in network engineering, fault-tolerant system design, and OPSEC.*

---

### Rozproszony System Zarządzania Agentami (PL)

Praktyczny dashboard klasy Command & Control (C2) z interfejsem webowym, napisany w Node.js przy użyciu Socket.IO. Aplikacja automatyzuje wdrażanie agentów w środowiskach zdalnych, zarządza routingiem sieciowym w celu uniknięcia detekcji oraz zapewnia monitorowanie wszystkich instancji w czasie rzeczywistym.

#### Jak to działa?

**Zarządzanie Agentami i Automatyzacja**
* Dynamicznie powołuje do życia i zarządza dziesiątkami zautomatyzowanych instancji (botów) z poziomu scentralizowanego panelu web.
* Wykorzystuje złożone maszyny stanu do obsługi wyzwań serwerowych i omijania weryfikacji anty-botowych bez ingerencji człowieka.
* Automatyzuje rutynowe zadania i akcje w docelowym środowisku.

**Routing Sieciowy (OPSEC)**
* Integruje dynamiczny routing przez proxy SOCKS5, aby maskować oryginalny adres IP każdego agenta.
* Zapobiega blokadom IP (blacklisting) i symuluje naturalny, rozproszony ruch sieciowy.

**Odporność na Awarie i Monitorowanie**
* Posiada wbudowany mechanizm "watchdog" monitorujący stan zdrowia agentów.
* Automatycznie eliminuje zawieszone procesy (tzw. zombie) i inicjuje procedury ponownego łączenia w przypadku nieoczekiwanego rozłączenia.

**Dashboard C2 i Telemetria**
* Dwukierunkowa komunikacja w czasie rzeczywistym z wykorzystaniem WebSockets (`socket.io`).
* Wyświetla na żywo logi systemowe, status połączeń agentów oraz metryki sprawności serwerów proxy.
* Pozwala na masowe wykonywanie poleceń lub precyzyjne sterowanie pojedynczymi agentami.

**Powiadomienia (Alerting)**
* Zintegrowano API Discorda do wysyłania alertów o zdarzeniach krytycznych w czasie rzeczywistym (np. awarie proxy, restarty serwera, błędy agentów).

#### Wymagania / Technologie
* Node.js, Express
* Socket.IO (WebSockets)
* Discord.js
* Zarządzanie ruchem SOCKS5 Proxy

#### Zalecenia bezpieczeństwa
* Zaprezentowana architektura demonstruje techniki szeroko wykorzystywane w działaniach Red Teamingu oraz zaawansowanej automatyzacji.
* Omawiane mechanizmy powinny być stosowane wyłącznie w środowiskach, których jesteś właścicielem lub posiadasz wyraźną zgodę na ich testowanie.

*Projekt pokazuje praktyczne umiejętności z zakresu inżynierii sieciowej, projektowania systemów odpornych na awarie (Fault Tolerance) oraz OPSEC.*
