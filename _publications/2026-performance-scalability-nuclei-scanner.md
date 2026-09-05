---
title: "Performance and Scalability Evaluation of the Nuclei Vulnerability Scanner Under Different Execution Architectures"
collection: publications
category: manuscripts
permalink: /publication/2026-performance-scalability-nuclei-scanner
excerpt: 'An empirical evaluation of execution strategies (sequential, multithreaded, and multiprocess) characterizing throughput, resource utilization, and architectural scaling bottlenecks for template-driven security workloads on multi-core systems.'
date: 2026-09-01
venue: 'Manuscript in Preparation'
citation: '<b>Hannan Ali</b> (2026). &quot;Performance and Scalability Evaluation of the Nuclei Vulnerability Scanner Under Different Execution Architectures.&quot; <i>Manuscript in preparation ahead of conference submission</i>.'
---

{% include base_path %}

### Overview & Status
- **Author:** Hannan Ali
- **Status:** Manuscript complete; under advisor review ahead of academic conference submission.
- **Target Venues:** Computer Systems & Security Conferences / Workshops.

---

### Abstract
Template-driven vulnerability scanners such as Nuclei are critical components of modern automated security analysis pipelines. However, their execution behavior and scalability characteristics across concurrency models remain largely uncharacterized in empirical literature. This work presents a rigorous performance evaluation of the Nuclei scanner across three execution paradigms—**sequential**, **multithreaded (goroutine worker pools)**, and **parallel-process execution**—under controlled workloads on multi-core hardware. 

Through instrumented benchmark trials measuring wall-clock execution time, CPU utilization, resident set size (RSS) memory consumption, and network I/O throughput, we identify key scaling limits and architectural bottlenecks. We apply non-parametric hypothesis testing (Kruskal–Wallis and Mann–Whitney $U$) to validate performance disparities across concurrency tiers, demonstrating where process-level concurrency incurs diminishing returns relative to thread-level multiplexing under heavy I/O contention.

---

### Experimental Methodology & Architecture

1. **Controlled Benchmarking Harness:**
   - Designed a reproducible benchmarking harness that automates experiment orchestration, metrics collection, and statistical aggregation across repeated trials under fixed target workloads.
   - Evaluated scaling sweeps over concurrency levels (from single-worker baselines up to high concurrency limits).

2. **Instrumented Metrics:**
   - **Latency & Wall-Clock Duration:** Elapsed scan time across homogeneous and heterogeneous template sets.
   - **Throughput:** HTTP request dispatch and template evaluation rates (req/sec).
   - **Resource Overhead:** Per-core CPU utilization curves, peak resident set size (RSS), and memory footprint growth.
   - **I/O & Concurrency Behavior:** Network connection pooling dynamics, socket exhaustion thresholds, and scheduler overhead.

3. **Statistical Grounding:**
   - Used non-parametric statistical tests (**Kruskal–Wallis**, **Mann–Whitney $U$**) to establish statistical significance of performance differences without assuming normal distribution of latency profiles.

---

### Key Empirical Findings

| Execution Paradigm | Scalability Characteristics | Memory Behavior | Primary Bottleneck |
| :--- | :--- | :--- | :--- |
| **Sequential Baseline** | Linear time complexity relative to template count; predictable execution envelope. | Low, constant RSS footprint. | Complete CPU/network under-utilization. |
| **Multithreaded / Worker Pool** | Near-linear throughput gains at moderate concurrency levels; optimal resource efficiency. | Modest memory scaling; efficient goroutine stack allocations. | Socket multiplexing & connection pool contention at high concurrency. |
| **Multiprocess Execution** | High isolation between scanner instances; effective for fault-tolerant partitioning. | Substantial RSS overhead due to duplicate runtime and template state per process. | Inter-process I/O contention and operating system scheduler context switching. |

---

### Contributions
- **Empirical Baseline:** A quantitative characterization of template-driven vulnerability scanning performance across execution models on modern multi-core systems.
- **Bottleneck Localization:** Identification of memory scaling profiles and I/O multiplexing thresholds governing scanner efficiency.
- **Reproducible Artifacts:** An open-source benchmarking suite and harness allowing researchers and practitioners to systematically evaluate scanning workloads.
