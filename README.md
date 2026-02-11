# Hi, I'm Won 👋

> **Backend Engineer & System Architect**
> *Building scalable, server-driven architectures for real-life solutions.*

I specialize in designing **robust backend systems** that ensure data consistency across distributed clients.
Currently building **Project OHANA**, a private family ERP system, bridging **Spring Boot** logic with **Expo** mobile experiences.

---

### 🔭 Featured Architecture: Project OHANA
**"Reliable Logic, Fluid Experience."**

OHANA is designed with a **"Thick Server, Thin Client"** philosophy.
The **Expo (React Native)** app serves as a responsive interface, while the **Spring Boot** core handles complex state management, idempotency, and 3rd-party integrations (Google Workspace).

```mermaid
graph LR
    subgraph "Client Layer (Expo)"
        User((Family)) -->|Touch/Input| App[Mobile App]
        App -->|REST API| Gateway[API Gateway]
    end

    subgraph "Server Core (Spring Boot)"
        Gateway -->|Logic| Service[Domain Service]
        Service -->|Auth| Supabase[Supabase Auth]
        Service -->|Data| DB[(PostgreSQL)]
        Service -->|Async| Batch[Spring Batch]
    end
    
    subgraph "Integration"
        Batch -->|OAuth2| GSheets[Google Sheets]
        GSheets -->|Sync| Logs[Feeding/Care Logs]
    end
🛠 Tech StackDomainTechnologiesBackend CoreClient EngineInfra & DevOpsSecurity🚀 Engineering Logs (Latest Thoughts)I document my architectural decisions and troubleshooting journeys.Moving Logic to the Server: The OHANA Refactor ✨ (Featured)Designing Idempotent APIs for Mobile ClientsSecure Token Management with AES-GCM👉 Read more at won-hope.github.io📊 GitHub Stats<div align="center"><img src="https://www.google.com/search?q=https://github-readme-stats.vercel.app/api%3Fusername%3Dwon-hope%26theme%3Dmonokai%26hide_border%3Dtrue%26include_all_commits%3Dtrue%26count_private%3Dtrue%26show_icons%3Dtrue" height="150" alt="stats graph" /><img src="https://www.google.com/search?q=https://nirzak-streak-stats.vercel.app/%3Fuser%3Dwon-hope%26theme%3Dmonokai%26hide_border%3Dtrue" height="150" alt="streak graph" /></div><div align="center"><a href="https://visitcount.itsvg.in"><img src="https://visitcount.itsvg.in/api?id=won-hope&icon=0&color=5" /></a></div>
