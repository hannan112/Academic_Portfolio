---
title: "DistInfer: High-Throughput Distributed LLM Serving Engine"
excerpt: "A lightweight distributed serving engine featuring continuous batching, paged attention, and pipeline parallel KV-cache migration.<br/><br/><b>Tech:</b> Python, PyTorch, C++, Triton, FastAPI"
collection: portfolio
---

### Overview
DistInfer is a fast, modular LLM inference and serving platform designed for multi-GPU edge nodes and cloud clusters. It achieves high serving throughput and sub-second time-to-first-token (TTFT) by utilizing dynamic request scheduling and optimized memory management.

### Key Capabilities
- **Continuous Batching:** Dynamically batches incoming prompt and decode phases.
- **Paged Attention & KV-Cache Sharing:** Drastically reduces memory fragmentation across heterogeneous GPU configurations.
- **Microservice Architecture:** REST and WebSocket endpoints for seamless integration into production workflows.

### Resources
- [GitHub Repository](https://github.com/)
- [Benchmarks & Performance Plots](https://github.com/)
