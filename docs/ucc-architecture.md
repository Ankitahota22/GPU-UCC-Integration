# UCC Architecture and Interface Investigation

## 1. Introduction

UCC was studied as a separate memory-system simulation framework during the internship. The objective was to understand its architecture, memory hierarchy, and communication interfaces before exploring possible integration with GPGPU-Sim.

## 2. Important Source Files

| Source File | Purpose Investigated |
|---|---|
| `GPUMemoryHierarchy.hpp` | GPU memory hierarchy interface |
| `GPUMemoryHierarchy.cpp` | GPU memory hierarchy implementation |
| `MemoryHierarchy.hpp` | Memory hierarchy declarations |
| `MemoryHierarchy.cpp` | Memory hierarchy implementation |
| `FetchInterface.cpp` | Instruction-fetch interface |
| `LoadStoreInterface.cpp` | Load/store interface |
| `RequestController.*` | Request-control components |

## 3. FetchInterface

FetchInterface was investigated to understand the instruction-fetch communication path.

The previously recorded interface components included:

- CoreConfig
- SlavePort
- MasterPort
- RequestPool
- TraceReader
- SimConfig
- MemoryHierarchy

The interface also contained ports related to fetch requests, responses, write data, and probe requests.

## 4. Fetch Execution Workflow

The recorded fetch workflow included a clock-cycle function named `f_clockCycle()`.

The previously studied execution sequence involved:

1. Watchdog handling.
2. Retirement.
3. Execution.
4. Instruction issue.
5. Decode.
6. Fetch.

The function `f_fetchTransaction()` was also examined as part of the fetch transaction investigation.

## 5. LoadStoreInterface

LoadStoreInterface was studied to understand how data-memory operations interact with UCC's memory hierarchy.

The investigation focused on the interface's role in handling load/store requests and communication with memory-system components.

## 6. MemoryHierarchy

The `MemoryHierarchy` components were examined to understand how requests interact with the underlying memory-system model.

The `GPUMemoryHierarchy` files were also explored to understand the GPU-specific hierarchy interface.

## 7. Importance to the Internship

Studying these interfaces helped identify the components that could potentially communicate with GPGPU-Sim.

The FetchInterface was particularly relevant to the investigation of instruction-fetch integration, while LoadStoreInterface was relevant to data-memory access.

## 8. Summary

The UCC investigation provided an understanding of its memory hierarchy and interface organization. This knowledge supported further investigation into connecting a GPU simulator with an alternative memory-system model.

**Note:** This document records the components and workflow investigated. It does not claim that every interface was fully integrated or experimentally validated.