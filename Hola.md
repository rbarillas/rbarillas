flowchart TD
    %% Start and End Nodes
    Start([Inicio del Proceso])
    End([Fin del Proceso])

    %% Identificación del Conflicto
    Start --> A[Identificación del Conflicto<br>(Art. 1, 8, 9)]
    A --> B{¿Tipo de Conflicto?<br>(Art. 1, 8)}
    B -->|Conflicto: Tribunal vs. Administración Pública| C[Planteamiento del Conflicto<br>(Art. 8, 9)]
    B -->|Conflicto: Tribunal vs. Tribunales Ordinarios| C
    B -->|Conflicto: Administración Pública vs. Tribunales Ordinarios| C

    %% Planteamiento del Conflicto
    C --> D[Envío de Solicitud al Tribunal<br>Plazo: 5 días<br>(Art. 9)]
    D --> E[Recepción de Documentos<br>Plazo: 48 horas<br>(Art. 10)]
    E --> F{¿Documentación Completa?<br>(Art. 10)}
    F -->|Sí| G[Evaluación de Documentos<br>(Art. 10)]
    F -->|No| H[Requerir Documentación Adicional<br>Plazo: 48 horas<br>(Art. 10)]
    H --> D %% Loop back if additional documents are required

    %% Evaluación y Decisión del Tribunal
    G --> I[Integración del Tribunal<br>(Art. 2)]
    I --> J[Evaluación del Conflicto<br>(Art. 11)]
    J --> K{Decisión sobre Competencia<br>(Art. 11, 13)}
    K -->|Competencia: Administración Pública| L[Asignar a Administración Pública<br>(Art. 11, 13)]
    K -->|Competencia: Tribunales Ordinarios| M[Asignar a Tribunales Ordinarios<br>(Art. 11, 13)]
    K -->|Competencia: Tribunal de lo Contencioso| N[Asignar a Tribunal Contencioso<br>(Art. 11, 13)]

    %% Notificación y Registro
    L --> O[Notificación de Decisión a Partes<br>(Art. 14)]
    M --> O
    N --> O
    O --> P{¿Todas las Partes Notificadas?<br>(Art. 14)}
    P -->|Sí| Q[Registrar Resolución<br>(Art. 15)]
    P -->|No| O
    Q --> R[Control de Dietas para Magistrados<br>(Art. 15)]
    R --> End

    %% Styling for clarity
    style Start fill:#66c2ff,stroke:#333,stroke-width:2px
    style End fill:#66c2ff,stroke:#333,stroke-width:2px
    style A fill:#ffcc66,stroke:#333,stroke-width:2px
    style B fill:#ffcc66,stroke:#333,stroke-width:2px
    style C fill:#ff9966,stroke:#333,stroke-width:2px
    style D fill:#66ff66,stroke:#333,stroke-width:2px
    style E fill:#66ff66,stroke:#333,stroke-width:2px
    style F fill:#ffcc66,stroke:#333,stroke-width:2px
    style G fill:#66ff66,stroke:#333,stroke-width:2px
    style H fill:#ff9966,stroke:#333,stroke-width:2px
    style I fill:#ffcc66,stroke:#333,stroke-width:2px
    style J fill:#66ff66,stroke:#333,stroke-width:2px
    style K fill:#ffcc66,stroke:#333,stroke-width:2px
    style L fill:#66ff66,stroke:#333,stroke-width:2px
    style M fill:#66ff66,stroke:#333,stroke-width:2px
    style N fill:#66ff66,stroke:#333,stroke-width:2px
    style O fill:#ff9966,stroke:#333,stroke-width:2px
    style P fill:#ffcc66,stroke:#333,stroke-width:2px
    style Q fill:#66ff66,stroke:#333,stroke-width:2px
    style R fill:#66ff66,stroke:#333,stroke-width:2px
