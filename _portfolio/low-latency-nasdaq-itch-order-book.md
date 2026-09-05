---
title: "Low-Latency Order Book for NASDAQ ITCH Market Data"
excerpt: "A cache-conscious, zero-allocation limit order book in modern C++ engineered for sub-microsecond NASDAQ TotalView-ITCH 5.0 feed processing."
collection: portfolio
date: 2026-02-01
---

Independent systems research & performance engineering project (2025 – 2026).

### Motivation
In high-frequency market data pipelines and electronic execution platforms, per-message processing latency—rather than aggregate throughput—is the binding constraint. Real-world financial feeds like NASDAQ TotalView-ITCH 5.0 transmit millions of discrete order book updates per second during market volatility. At these message rates, traditional object-oriented designs suffer from unpredictable latency spikes caused by heap allocation overhead, pointer chasing across fragmented memory, and CPU cache misses.

This project investigates how data-oriented design, memory layout alignment, and zero-allocation strategies in modern C++ optimize memory hierarchy utilization and minimize tail latency under heavy message rates.

---

### Key Architectural & Systems Decisions

* **Data-Oriented Layout & Cache Locality:**
  - Designed memory-aligned, packed structures for order records to fit critical order metadata within single CPU cache lines (64 bytes).
  - Replaced pointer-heavy tree structures with contiguous memory arrays and flat indexed price levels, eliminating pointer indirection on the hot path.

* **Zero Dynamic Allocations on Hot Path:**
  - Implemented pre-allocated object pools and slab allocators for active orders and price levels, ensuring that order additions, executions, and cancellations perform no dynamic heap allocations (`malloc`/`free` or `new`/`delete`) during message processing.

* **Binary Protocol Parsing (Zero-Copy):**
  - Built a zero-copy binary parser for NASDAQ TotalView-ITCH 5.0 specification messages, handling order additions (Type `A`, `F`), order executions (Type `E`, `C`), cancellations (Type `X`), deletions (Type `D`), and replaces (Type `U`).

* **Fast $O(1)$ Order Lifecycle Operations:**
  - Utilized intrusive doubly linked lists per price level combined with direct-indexed lookups to achieve $O(1)$ time complexity for order lookup, queue insertion, and cancellation.

---

### Performance Profiling & Evaluation

We instrumented the pipeline using hardware performance counters via Linux `perf` to evaluate the architectural impact of memory layout decisions under high-rate historical ITCH message traces:

| Metric / Aspect | Conventional Pointer-Based Design | Data-Oriented & Pool-Allocated Design | Architectural Impact |
| :--- | :--- | :--- | :--- |
| **Hot-Path Allocations** | Dynamic heap allocation per order event | **Zero runtime allocations** (pre-allocated pool) | Eliminates allocator lock contention & heap fragmentation |
| **L1 Data Cache Misses** | High (frequent pointer dereferencing) | **Substantially reduced** (contiguous struct layout) | Maximizes memory bandwidth and cache line residency |
| **Branch Mispredictions** | High (polymorphic dispatch & branches) | **Minimized** (predictable branch layout & fast paths) | Improves Instructions Per Cycle (IPC) |
| **Per-Message Latency** | Non-deterministic with long tails | **Deterministic sub-microsecond median latency** | Strict bound on tail latency under market bursts |

---

### Tech Stack & Tooling
**Language:** C++20  
**Systems & APIs:** Linux, POSIX, Memory Alignment, Cache Line Padding  
**Profiling & Benchmarking:** Linux `perf`, Google Benchmark, Valgrind / Cachegrind  
**Toolchain:** GCC, Clang, CMake, GTest
