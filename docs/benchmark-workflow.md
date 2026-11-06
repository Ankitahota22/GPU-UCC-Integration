# CUDA Benchmark Execution Workflow

## 1. Introduction

CUDA benchmarks were used during the internship to understand GPU program execution within the GPGPU-Sim simulation environment.

The main workloads discussed in the project were VectorAdd and MatrixMul.

## 2. Development Environment

The benchmark workflow involved:

- Linux-based development environment.
- Docker container for environment isolation.
- CUDA toolkit and compiler.
- GPGPU-Sim simulator.
- Benchmark source files and execution scripts.

## 3. VectorAdd Benchmark

VectorAdd is a basic CUDA workload that performs element-wise addition of two input vectors.

For two vectors A and B, the output vector C is calculated as:

C[i] = A[i] + B[i]

This benchmark provides a simple workload for examining GPU kernel execution and memory access behavior.

## 4. MatrixMul Benchmark

MatrixMul performs matrix multiplication using GPU parallel processing.

For matrices A and B, the resulting matrix C is calculated as:

C[i][j] = Σ A[i][k] × B[k][j]

This workload provides an opportunity to study parallel computation and memory access patterns.

## 5. Execution Workflow

The general workflow investigated during the internship was:

1. Prepare the development environment.
2. Configure GPGPU-Sim.
3. Prepare CUDA benchmark source files.
4. Compile the benchmark programs.
5. Configure the simulation environment.
6. Execute the workloads.
7. Monitor benchmark execution.
8. Inspect available logs and memory-related outputs.

### Figure 1: Conceptual Benchmark Workflow

```text
+----------------------+
| Environment Setup    |
+----------+-----------+
           |
           v
+----------------------+
| GPGPU-Sim Setup      |
+----------+-----------+
           |
           v
+----------------------+
| CUDA Benchmark       |
| Preparation          |
+----------+-----------+
           |
           v
+----------------------+
| Compilation          |
+----------+-----------+
           |
           v
+----------------------+
| Simulation Execution |
+----------+-----------+
           |
           v
+----------------------+
| Monitoring and       |
| Output Investigation |
+----------------------+
```

*Note: This is a conceptual representation of the workflow.*

## 6. Execution Monitoring

The internship workflow also involved examining benchmark execution and monitoring processes.

The purpose was to understand execution progress and investigate simulation-related outputs.

## 7. Trace and Memory-Dump Investigation

Memory-related traces and memory-dump outputs were explored to understand how simulation activity could be inspected.

These outputs can help investigate memory requests and simulator behavior.

## 8. Summary

The benchmark work provided practical exposure to CUDA workloads, simulation configuration, execution monitoring, and memory-related investigation.

**Note:** This document describes the workflows studied. Exact execution times, benchmark counts, and performance measurements are not reported because verified result files are not currently available in this personal repository.