# Architecture

```mermaid
flowchart TD
    subgraph MobileApp["Mobile App (Flutter/Dart)"]
        UI["User Interface<br>(Flutter Widgets)"]
        BL["Business Logic<br>(Dart Services)"]
        APIClient["API Client<br>(Dio/HTTP)"]
    end

    subgraph Backend["Supabase Backend"]
        DB["Postgres Database"]
        Auth["Auth Service"]
        RPC["Edge Functions<br>(Serverless)"]
    end

    subgraph Payments["Nayax Payment API"]
        NayaxAPI["Nayax REST API<br>(Payments & Transactions)"]
    end

    %% Mobile app internals
    UI -->|User actions & events| BL
    BL -->|Data requests & responses| APIClient

    %% Supabase interactions
    APIClient -->|Login / Token exchange| Auth
    APIClient -->|"CRUD operations (SQL queries)"| DB
    APIClient -->|Trigger serverless logic| RPC

    %% Nayax interaction
    BL -->|Initiate payments / Get status| NayaxAPI

    %% Relationships inside Supabase
    Auth -->|Verify identity & permissions| DB
    RPC -->|Query & update data| DB
    RPC -->|Secure payment validation| NayaxAPI

```

## Modules
### Mobile App (Flutter/Dart)
- User Interface (Flutter Widgets): Handles rendering of screens, navigation, and user interactions.
- Business Logic (Dart Services): Encapsulates application rules, state management, validation, and coordinates data flow between UI and backend services.
- API Client (Dio/HTTP): Manages network communication, sending requests and receiving responses from Supabase and the Nayax API.

### Supabase Backend
- Postgres Database: Stores structured data such as user profiles, app entities, and transaction records.
- Auth Service: Provides secure authentication, authorization, and user identity management.
- Edge Functions (Serverless): Executes custom backend logic like payment validation, data transformations, and secure workflows.

### Nayax Payment API
- Nayax REST API (Payments & Transactions): Handles financial transactions, including payment initiation, processing, and verification, ensuring secure integration with external payment systems.
