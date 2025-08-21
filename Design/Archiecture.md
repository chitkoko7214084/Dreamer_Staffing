graph TD
    subgraph "Frontend (Vue.js Application)"
        A[Applicant Web App]
        B[Staff Dashboard]
    end

    subgraph "Firebase Backend"
        subgraph "Authentication & Authorization"
            C[Firebase Authentication]
        end
        subgraph "Database"
            D[Cloud Firestore]
        end
        subgraph "Serverless Functions"
            E[Cloud Functions]
        end
    end

    A -- "1. Submits Data (Application)" --> C & D
    B -- "2. Reads & Manages Data" --> D
    D -- "3. Data Change Trigger" --> E
    E -- "4. Logic: Calculate Score & Categorize" --> D
    C -- "5. Secures Data Access via Rules" --> D
