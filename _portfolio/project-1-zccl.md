---
title: "ZCCL: Compression-Accelerated Collective Communication Library"
excerpt: "A high-performance GPU and CPU collective communication library with integrated real-time lossy and lossless data compression algorithms.<br/><br/><b>Tech:</b> C++, CUDA, MPI, NCCL, RDMA"
collection: portfolio
---

### Overview
ZCCL is an open-source research initiative designed to mitigate network bottlenecks in distributed machine learning and scientific high-performance computing. It integrates compression pipelines directly into collective primitives (such as `AllReduce`, `AlltoAll`, and `ReduceScatter`).

### Key Capabilities
- **End-to-End Pipeline:** Seamless integration with PyTorch DDP and DeepSpeed.
- **Hardware Acceleration:** Native CUDA kernels and Tensor Core optimizations for zero-latency compression overhead.
- **Adaptive Error Control:** Dynamically adjusts compression tolerances to guarantee target convergence accuracy.

### Resources
- [GitHub Repository](https://github.com/)
- [Documentation & Benchmarks](https://github.com/)
- [Related Research Paper](/publication/2026-high-throughput-deep-learning)
