# Hi there, I'm Won 👋

> **Backend Engineer & System Architect**
> *Building scalable, high-availability systems for real-life problem solving.*

I focus on **robust architecture**, **automation**, and **data consistency**.
Currently building a **Private Family ERP System** to optimize infant care workflows.

---

### 🔭 Featured Architecture: Project OHANA
**"Data-Driven Parenting: Automating the unseen labor of childcare."**

OHANA is a centralized ERP system integrating mobile clients with Google Workspace. It ensures **idempotency** in distributed environments and secures sensitive family data with **AES-GCM encryption**.

```mermaid
graph LR
    User((Family)) -->|Mobile App| Client[Expo/React Native]
    Client -->|REST API| Server[Spring Boot 3.x]
    
    subgraph "OHANA Core (Backend)"
        Server -->|Auth| Supabase[Supabase Auth]
        Server -->|Data| DB[(PostgreSQL)]
        Server -->|Batch| Scheduler[Spring Batch]
    end
    
    subgraph "External Integrations"
        Scheduler -->|OAuth2| GSheets[Google Sheets API]
        GSheets -->|Export| Report[Daily Reports]
    end
