# GPU Memory Hierarchy Analysis and UCC Integration with GPGPU-Sim

**Internship Project | IIT Bhubaneswar**

A technical documentation repository covering GPU memory hierarchy analysis, GPGPU-Sim source-code investigation, CUDA benchmark workflows, and exploration of UCC integration.

## About the Project

This repository documents the technical work carried out during my 45-day internship at the Indian Institute of Technology (IIT) Bhubaneswar under the supervision of Dr. Debiprasanna Sahoo.

The work focused on understanding GPU memory hierarchy, investigating cache access mechanisms in GPGPU-Sim, executing CUDA benchmarks, and studying UCC as an alternative memory-system simulation framework.

## Internship Details

| Category | Information |
|---|---|
| Organization | IIT Bhubaneswar |
| Supervisor | Dr. Debiprasanna Sahoo |
| Duration | 45 Days |
| Completion Date | 30 June 2026 |
| Project Domain | GPU Simulation and Computer Architecture |
| Technologies | C++, CUDA, GPGPU-Sim, UCC, Docker, Linux |

## Objectives

- Understand GPU architecture and memory hierarchy.
- Investigate L1 Instruction Cache (L1I), L1 Data Cache (L1D), and L2 cache.
- Study GPGPU-Sim source-code organization and cache access paths.
- Prepare and execute CUDA benchmarks such as VectorAdd and MatrixMul.
- Explore simulation monitoring and memory-related outputs.
- Investigate UCC memory hierarchy and its FetchInterface and LoadStoreInterface.
- Explore possible integration approaches between UCC and GPGPU-Sim.

## Technologies and Tools

- **GPGPU-Sim:** GPU architecture simulation.
- **UCC:** Memory-system simulation framework.
- **CUDA:** GPU programming and benchmark execution.
- **C++:** Source-code investigation.
- **Docker:** Containerized development environment.
- **Linux:** Development and simulation environment.
- **Git and GitHub:** Version control and documentation.

## Repository Structure

```text
GPU-UCC-Integration/
│
├── README.md
│
├── docs/
│   ├── project-overview.md
│   ├── gpu-memory-hierarchy.md
│   ├── gpgpu-sim-source-analysis.md
│   ├── ucc-architecture.md
│   ├── integration-investigation.md
│   ├── benchmark-workflow.md
│   ├── limitations-and-future-work.md
│   └── references.md
│
├── diagrams/
│   ├── gpu-memory-hierarchy.md
│   ├── ucc-integration-flow.md
│   └── benchmark-workflow.md
│
└── evidence/
```text

## Technical Areas Investigated

### 1. GPU Memory Hierarchy

Study of registers, shared memory, L1 instruction cache, L1 data cache, L2 cache, and global memory.

### 2. GPGPU-Sim Source-Code Analysis

Investigation of important source files:

- `shader.cc`
- `gpu-cache.cc`
- `l2cache.cc`

### 3. UCC Architecture

Study of:

- `FetchInterface.cpp`
- `LoadStoreInterface.cpp`
- `MemoryHierarchy.cpp`
- `GPUMemoryHierarchy.cpp`

### 4. Benchmark Workflow

Investigation of CUDA benchmark preparation and execution using VectorAdd and MatrixMul, along with execution monitoring and memory-related output analysis.

### 5. Integration Investigation

Exploration of possible communication between GPGPU-Sim and UCC through their memory-system interfaces, particularly the instruction-fetch path.

## Code Availability and Research Context

The internship work was carried out in an IIT Bhubaneswar research environment as part of an ongoing project under faculty supervision.

The original development environment and project source code were maintained within that research environment and are not included in this personal repository. This repository therefore focuses on documenting the concepts studied, source-level investigations, simulation workflows, integration approach, and technical learning outcomes.

No proprietary or unpublished research code is reproduced here.

## Documentation

Detailed project documentation:

| Document | Description |
|---|---|
| [Project Overview](docs/project-overview.md) | Internship background, objectives, and scope |
| [GPU Memory Hierarchy](docs/gpu-memory-hierarchy.md) | GPU memory components and organization |
| [GPGPU-Sim Source Analysis](docs/gpgpu-sim-source-analysis.md) | Cache implementation investigation |
| [UCC Architecture](docs/ucc-architecture.md) | UCC interfaces and memory hierarchy |
| [Integration Investigation](docs/integration-investigation.md) | Explored integration approach |
| [Benchmark Workflow](docs/benchmark-workflow.md) | CUDA benchmark execution workflow |
| [Limitations and Future Work](docs/limitations-and-future-work.md) | Current limitations and future directions |
| [References](docs/references.md) | Technical documentation and resources |

## Diagrams

- [GPU Memory Hierarchy](diagrams/gpu-memory-hierarchy.md)
- [UCC Integration Flow](diagrams/ucc-integration-flow.md)
- [Benchmark Workflow](diagrams/benchmark-workflow.md)

## Limitations

This repository is a documentation-based record of internship work. Original server-side source files and complete experimental records are not currently available for independent verification.

The integration approach is documented as an investigation, not as a claim of complete cache-hierarchy replacement or experimentally demonstrated performance improvement.

## Future Work

- Further development of the UCC–GPGPU-Sim integration.
- Validation of memory request and response communication.
- Detailed cache behavior experiments.
- Reproducible benchmark evaluation.
- Comparative memory-system performance analysis.

## Acknowledgement

I would like to acknowledge IIT Bhubaneswar and my internship supervisor, Dr. Debiprasanna Sahoo, for the opportunity to work on GPU memory hierarchy analysis and UCC integration concepts.

## Author

**Ankita Hota**

B.Tech – Computer Science and Engineering

Government College of Engineering, Kalahandi

## References

- [GPGPU-Sim Repository](https://github.com/accel-sim/gpgpu-sim_distribution)
- [Internship Research Repository](https://github.com/Nitesh8998/mlMem)
- [NVIDIA CUDA Documentation](https://docs.nvidia.com/cuda/)