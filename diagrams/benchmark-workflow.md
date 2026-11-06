flowchart TD
    A[Docker Environment]
    B[GPGPU-Sim Setup]
    C[CUDA Benchmark Preparation]
    D[VectorAdd / MatrixMul]
    E[Simulation Execution]
    F[Execution Monitoring]
    G[Trace / Memory Dump Investigation]
    H[Result Analysis]

    A --> B
    B --> C
    C --> D
    D --> E
    E --> F
    F --> G
    G --> H