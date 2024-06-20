graph TD
    subgraph "Frontend"
        A[React App]
        B[App.js]
        C[Login.js]
        D[VideoChat.js]
        E[Leaderboard.js]
        F[Profile.js]
    end

    subgraph "Backend Services"
        G[Azure Functions]
        H[SignalR Service]
        I[WebRTC]
    end

    subgraph "External Services"
        J[Azure Cosmos DB]
        K[Azure Blob Storage]
        L[Azure Key Vault]
        M[Azure Text Analytics]
        N[Firebase Auth]
        O[Firebase Firestore]
    end

    A --> B
    B --> C
    B --> D
    B --> E
    B --> F

    C --> N
    D --> I
    D --> H
    D --> M
    E --> O
    F --> O

    G --> J
    G --> K
    G --> L

    D --> G
    I --> H

    classDef frontend fill:#d5e8d4,stroke:#82b366;
    classDef backend fill:#dae8fc,stroke:#6c8ebf;
    classDef external fill:#fff2cc,stroke:#d6b656;

    class A,B,C,D,E,F frontend;
    class G,H,I backend;
    class J,K,L,M,N,O external;
