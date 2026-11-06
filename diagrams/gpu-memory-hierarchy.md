# GPU Memory Hierarchy

```mermaid
flowchart TD
    A[CUDA Application] --> B[Streaming Multiprocessor]
    B --> C[Registers]
    B --> D[Shared Memory]
    B --> E[L1 Instruction Cache]
    B --> F[L1 Data Cache]
    E --> G[L2 Cache]
    F --> G
    G --> H[Global Memory / GPU DRAM]