flowchart TD
    A[GPU Application / CUDA Kernel]
    B[Streaming Multiprocessor - SM]
    C[Registers]
    D[Shared Memory]
    E[L1 Instruction Cache - L1I]
    F[L1 Data Cache - L1D]
    G[L2 Cache]
    H[Global Memory - GPU DRAM]

    A --> B
    B --> C
    B --> D
    B --> E
    B --> F
    E --> G
    F --> G
    G --> H