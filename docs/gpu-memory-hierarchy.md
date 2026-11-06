# GPU Memory Hierarchy

## 1. Introduction

A Graphics Processing Unit (GPU) is designed to execute a large number of operations in parallel. To support efficient execution, GPUs use a hierarchical memory organization that provides different levels of storage with different capacities, access latencies, and purposes.

Understanding this hierarchy is important for analyzing memory access behavior in GPU simulators such as GPGPU-Sim.

## 2. Overview of GPU Memory Hierarchy

The major memory components considered in this project are:

- Registers
- Shared Memory
- L1 Instruction Cache (L1I)
- L1 Data Cache (L1D)
- L2 Cache
- Global Memory (GPU DRAM)

### Figure 1: Conceptual GPU Memory Hierarchy

```text
             GPU Streaming Multiprocessor
          +-------------------------------+
          |          Registers            |
          +-------------------------------+
          |          Shared Memory        |
          +-------------------------------+
          |                               |
          |  +-----------+  +-----------+  |
          |  |   L1I     |  |   L1D     |  |
          |  | Instruction| |   Data    |  |
          |  |   Cache   |  |   Cache   |  |
          |  +-----------+  +-----------+  |
          +---------------+---------------+
                          |
                          v
                  +---------------+
                  |    L2 Cache   |
                  +---------------+
                          |
                          v
                  +---------------+
                  | Global Memory|
                  |    (DRAM)     |
                  +---------------+
```

*Note: This is a conceptual illustration of GPU memory organization. Exact cache configurations and sharing arrangements depend on the GPU architecture and simulator configuration.*

## 3. Registers

Registers are small, fast storage locations available to GPU threads. They hold temporary variables and intermediate computation results during kernel execution.

Their main purpose is to provide fast access to frequently used thread-local data.

## 4. Shared Memory

Shared memory is a programmer-managed memory space shared by threads within a thread block. It is commonly used to exchange data and reduce repeated accesses to global memory.

## 5. L1 Instruction Cache (L1I)

The L1 instruction cache stores recently fetched instructions. It helps reduce repeated instruction-fetch requests to lower levels of the memory hierarchy.

In GPGPU-Sim, the instruction-fetch path was investigated to understand how instruction requests interact with the L1 instruction cache.

## 6. L1 Data Cache (L1D)

The L1 data cache handles data-memory requests generated during GPU execution, depending on the configured cache and memory-access path.

The investigation focused on understanding how memory requests reach the cache and how cache operations are processed in GPGPU-Sim.

## 7. L2 Cache

The L2 cache is a lower-level cache that can serve requests from multiple GPU processing units. It reduces the need to access global memory for data that is already cached.

The L2 cache implementation was examined as part of the source-level memory hierarchy investigation.

## 8. Global Memory

Global memory is the main device memory accessible by GPU threads. It provides large storage capacity but generally has higher access latency than on-chip storage.

Efficient memory access patterns are important for GPU application performance.

## 9. Importance of Memory Hierarchy Analysis

Memory hierarchy analysis helps to:

1. Understand instruction and data access behavior.
2. Identify the roles of different cache levels.
3. Study memory request and response paths.
4. Investigate cache misses and lower-level memory accesses.
5. Understand how alternative memory-system models may interact with GPU simulators.

## 10. Relevance to the Internship

During the internship, the L1 instruction cache, L1 data cache, and L2 cache paths in GPGPU-Sim were investigated. This provided the background needed to study UCC interfaces and explore possible memory-system integration approaches.

## 11. References

Refer to the official GPGPU-Sim documentation and source-code references listed in `references.md`.