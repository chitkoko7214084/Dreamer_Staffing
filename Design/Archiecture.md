
graph TD
    subgraph "External Users"
        A[Applicant]
    end

    subgraph "Dreamer Staffing System"
        subgraph "Web Application"
            B[Frontend]
            C[Backend API]
        end
        subgraph "Core Services"
            D[Application Service]
            E[Assessment Service]
            F[Scoring & Categorization Service]
            G[Staff Management Service]
        end
        H[Database]
    end

    A -- "Submits Application & Tests" --> B
    B -- "Sends Data" --> C
    C -- "Handles Business Logic" --> D & E
    D -- "Saves Data" --> H
    E -- "Calculates Scores" --> F
    F -- "Stores Result" --> H
    F -- "Sends Category" --> C
    C -- "Retrieves Data" --> H
    C -- "Serves Data" --> B
    B -- "Presents Dashboard" --> G[Staff User]
    G -- "Views & Manages" --> C
