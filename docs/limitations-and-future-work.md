# Limitations and Future Work

## 1. Limitations

The internship work involved GPU memory hierarchy analysis and investigation of UCC integration with GPGPU-Sim. The following limitations apply to the currently documented work:

1. The original development environment was hosted on an IIT research server and is no longer accessible to me.
2. The original project source code is not included in this personal documentation repository.
3. Original benchmark logs and complete execution records are not currently available for independent verification.
4. The documented integration approach should not be interpreted as a fully validated replacement of the GPGPU-Sim cache hierarchy.
5. No new comparative performance measurements are presented in this repository.
6. Some architecture and workflow diagrams are conceptual explanations rather than screenshots of the original implementation.

## 2. Future Work

The following activities could extend the investigation:

### 2.1 Complete Integration Development

Further development could establish a working communication mechanism between GPGPU-Sim and UCC.

### 2.2 Request and Response Validation

Request formats, response handling, transaction identifiers, and synchronization mechanisms could be tested systematically.

### 2.3 Cache Behavior Analysis

Further experiments could investigate L1 instruction cache, L1 data cache, and L2 cache behavior under different workloads.

### 2.4 Benchmark Evaluation

VectorAdd and MatrixMul could be executed under controlled configurations to collect reproducible simulation results.

### 2.5 Performance Comparison

Future experiments could compare different memory-system configurations using verified metrics such as execution cycles, cache statistics, and memory latency.

### 2.6 Documentation and Reproducibility

A complete reproducibility guide could include environment requirements, build instructions, configuration details, and validated execution commands.

## 3. Conclusion

The internship established a foundation in GPU architecture simulation, memory hierarchy investigation, CUDA benchmark execution, and memory-system integration concepts.

Further implementation and experimental validation would help extend this work into a more complete integration study.