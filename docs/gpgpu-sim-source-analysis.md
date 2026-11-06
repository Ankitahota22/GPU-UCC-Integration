# GPGPU-Sim Source Code Analysis

## 1. Introduction

GPGPU-Sim is a cycle-level simulator used to study GPU architecture and execution behavior. During the internship, its source code was examined to understand how instruction fetching, data-memory requests, and cache operations are handled.

## 2. Source Files Investigated

| Source File | Area of Investigation |
|---|---|
| `shader.cc` | Shader core execution and memory access flow |
| `gpu-cache.cc` | Cache access, tag probing and request handling |
| `l2cache.cc` | L2 cache implementation |
| `l2cache.h` | L2 cache declarations and related structures |

## 3. L1 Instruction Cache (L1I)

The L1 instruction cache is involved in instruction fetching. The investigation focused on understanding how the shader core accesses the instruction cache and how instruction requests are processed.

The `shader.cc` source file was examined to identify the instruction-fetch path and the interaction with the L1 instruction cache.

## 4. L1 Data Cache (L1D)

The L1 data cache is involved in handling data-memory requests generated during kernel execution.

The investigation examined the memory-access flow in `shader.cc` and related cache operations implemented in `gpu-cache.cc`.

## 5. Cache Access Investigation

The following functions and operations were among the areas studied:

- `cache_access`
- `process_memory_access_queue`
- `l1_cache::access`
- `data_cache::access`
- `read_only_cache::access`
- `base_cache::access`
- `tag_array::probe`
- `send_read_request`
- `read_miss`

These functions were examined to understand cache access, tag checking, and memory request handling.

## 6. L2 Cache Investigation

The L2 cache implementation was studied through `l2cache.cc` and `l2cache.h`. The investigation focused on its role in the GPU memory hierarchy and its relationship with lower-level memory requests.

## 7. Relevance to UCC Integration

Understanding the existing cache access paths was important before exploring how UCC interfaces could interact with GPGPU-Sim.

The source-level investigation provided a foundation for identifying possible integration points, particularly around instruction fetching and memory requests.

## 8. Summary

The investigation provided practical exposure to GPGPU-Sim's internal source-code organization and cache access mechanisms. It helped identify the main source files relevant to GPU memory hierarchy analysis.

**Note:** This document describes source-level investigation. It does not claim that every cache function was modified or that the complete cache hierarchy was replaced.