flowchart TD
    A[GPGPU-Sim GPU Core]
    B[Instruction Fetch Request]
    C[Integration Interface]
    D[UCC FetchInterface]
    E[UCC Memory Hierarchy]
    F[Response Handling]
    G[GPU Core Receives Response]

    A --> B
    B --> C
    C --> D
    D --> E
    E --> F
    F --> G