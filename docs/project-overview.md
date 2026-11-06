# GPU Memory Hierarchy Analysis and UCC Integration with GPGPU-Sim

## 1. Project Overview

This project documents the technical work carried out during my internship at the Indian Institute of Technology (IIT) Bhubaneswar. The project focused on understanding GPU memory hierarchy, investigating cache operations in GPGPU-Sim, and exploring the integration of UCC as an alternative memory-system simulation framework.

The work involved studying GPU architecture, examining cache access paths in the GPGPU-Sim source code, executing CUDA benchmarks in a Docker-based simulation environment, and understanding the interfaces provided by UCC.

## 2. Internship Details

| Field | Details |
|---|---|
| Internship Organization | Indian Institute of Technology (IIT) Bhubaneswar |
| Project Title | GPU Memory Hierarchy Analysis and UCC Integration with GPGPU-Sim |
| Internship Duration | 45 Days |
| Completion Date | 30 June 2026 |
| Supervisor | Dr. Debiprasanna Sahoo |
| Domain | GPU Simulation, Computer Architecture and Memory Systems |

## 3. Problem Background

GPUs are designed to execute a large number of parallel operations. Their performance depends not only on computational resources but also on how efficiently data and instructions are accessed from memory.

A GPU memory hierarchy contains multiple levels of storage, including registers, shared memory, caches, and global memory. Understanding the behavior of these components is important when studying memory access patterns and simulation performance.

GPGPU-Sim provides a simulation environment for studying GPU architecture and execution behavior. UCC provides a separate memory-system simulation framework with its own interfaces and hierarchy.

Understanding the interaction between these systems requires examining their internal structures, request paths, and communication interfaces.

## 4. Project Objectives

The major objectives of the internship work were:

1. To understand GPU architecture and the GPU memory hierarchy.
2. To study GPGPU-Sim and its cache organization.
3. To investigate L1 Instruction Cache (L1I), L1 Data Cache (L1D), and L2 cache access paths.
4. To configure and work with a Docker-based GPGPU-Sim environment.
5. To prepare and execute CUDA benchmarks such as VectorAdd and MatrixMul.
6. To explore benchmark execution automation and monitoring.
7. To study UCC memory hierarchy components and interfaces.
8. To investigate a possible integration approach between UCC and GPGPU-Sim.

## 5. Scope of Work

The project covered the following areas:

- GPU memory hierarchy and cache organization.
- GPGPU-Sim source-code investigation.
- CUDA benchmark preparation and execution.
- Docker-based simulation environment.
- Execution monitoring and memory trace investigation.
- UCC architecture and interface study.
- Exploration of communication between GPGPU-Sim and UCC.

The scope of the documented work focuses on architectural understanding, source-level investigation, simulation workflows, and integration exploration.

## 6. Tools and Technologies

| Tool / Technology | Purpose |
|---|---|
| GPGPU-Sim | GPU architecture simulation |
| UCC | Memory-system simulation framework |
| CUDA | GPU programming and benchmark execution |
| Docker | Containerized development environment |
| Linux | Development and simulation environment |
| C++ | Simulator source-code investigation |
| Git and GitHub | Version control and project documentation |
| Visual Studio Code | Source-code and documentation editing |

## 7. Major Areas Investigated

### 7.1 GPGPU-Sim Cache Hierarchy

The investigation covered the L1 instruction cache, L1 data cache, and L2 cache. Source files such as `shader.cc`, `gpu-cache.cc`, and `l2cache.cc` were studied to understand cache access and request-handling paths.

### 7.2 CUDA Benchmark Execution

VectorAdd and MatrixMul were used as CUDA benchmark workloads during the simulation workflow. The work also involved examining execution automation, monitoring, and memory-related outputs.

### 7.3 UCC Interface Investigation

UCC components such as `FetchInterface.cpp`, `LoadStoreInterface.cpp`, and `MemoryHierarchy.cpp` were explored to understand how memory requests and responses are handled.

### 7.4 Integration Investigation

The project included investigating how UCC interfaces could communicate with GPGPU-Sim's memory and instruction-fetch paths. This involved studying the relevant source-level components and their possible interaction.

## 8. Project Outcome

The internship provided practical exposure to GPU architecture simulation, cache hierarchy investigation, CUDA benchmark execution, Docker-based development, and memory-system integration concepts.

The work helped develop an understanding of the internal organization of GPGPU-Sim and the interface structure of UCC. The integration investigation also provided a foundation for further research into connecting GPU simulators with alternative memory-system models.

## 9. Documentation Note

This repository is a personal documentation and research record of the internship work. It is being reconstructed using available project notes and previous technical discussions because the original development environment was hosted on an IIT server that is no longer accessible to me.

The documentation distinguishes investigated concepts and workflows from implementation results that have not been independently recovered or verified. It does not claim a complete replacement of the GPGPU-Sim cache hierarchy or experimentally demonstrated performance improvements.