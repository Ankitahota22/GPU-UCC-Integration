# UCC and GPGPU-Sim Integration Investigation

## 1. Introduction

The internship included investigating the possibility of connecting UCC with GPGPU-Sim to explore an alternative memory-system simulation approach.

GPGPU-Sim contains its own GPU execution and cache hierarchy mechanisms, whereas UCC provides separate memory-system interfaces. Understanding the communication between these systems was an important part of the project.

## 2. Integration Motivation

The integration investigation aimed to understand:

- How GPGPU-Sim generates instruction-fetch requests.
- How cache and memory requests are handled.
- How UCC receives and processes requests.
- How responses could be communicated between the systems.
- Which interfaces could serve as possible integration points.

## 3. Investigated Components

### GPGPU-Sim Components

- `shader.cc`
- `gpu-cache.cc`
- `l2cache.cc`

### UCC Components

- `FetchInterface.cpp`
- `LoadStoreInterface.cpp`
- `MemoryHierarchy.cpp`
- `GPUMemoryHierarchy.cpp`

## 4. Instruction-Fetch Integration Concept

The instruction-fetch path was an important area of investigation.

A bridge-based approach was explored to understand how GPGPU-Sim instruction-fetch activity could communicate with UCC's FetchInterface.

### Figure 1: Conceptual Integration Architecture

```text
+-----------------------+
|      GPGPU-Sim        |
|                       |
|   Shader Core         |
|       |               |
|       v               |
|   Instruction Fetch   |
+-----------+-----------+
            |
            v
+-----------------------+
|   Integration Bridge  |
|   (Conceptual Design) |
+-----------+-----------+
            |
            v
+-----------------------+
|    UCC FetchInterface |
|            |          |
|            v          |
|     MemoryHierarchy   |
+-----------------------+
```

*Note: This diagram illustrates the investigated integration concept, not a verified final implementation.*

## 5. Data-Memory Integration Considerations

The LoadStoreInterface was also studied to understand how data-memory operations might communicate with UCC.

Potential integration considerations included:

- Request translation.
- Address handling.
- Request identification.
- Response communication.
- Clock-cycle synchronization.
- Memory transaction management.

These points describe design considerations and should not be interpreted as completed implementation features.

## 6. Integration Challenges

Some important challenges associated with connecting two simulation frameworks include:

1. Differences in internal data structures.
2. Request and response format compatibility.
3. Clock-cycle synchronization.
4. Memory transaction management.
5. Maintaining correct instruction and data ordering.
6. Ensuring consistency between the two simulation models.

## 7. Investigation Outcome

The investigation improved understanding of the source-level components and interfaces that could participate in a UCC–GPGPU-Sim integration.

It also provided a conceptual foundation for further development of an integration bridge.

## 8. Conclusion

The work focused on understanding the existing simulator architecture and investigating possible integration paths. Complete integration and performance validation are not claimed in this documentation.