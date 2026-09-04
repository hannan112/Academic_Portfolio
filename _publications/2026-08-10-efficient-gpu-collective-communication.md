---
title: "Scalable Fault-Tolerant Distributed Memory Architectures for AI Clusters"
collection: publications
category: preprints
permalink: /publication/2026-scalable-fault-tolerant-distributed-memory
excerpt: 'A preprint presenting an asynchronous checkpointing and memory-sharing protocol for ultra-large distributed AI clusters.'
date: 2026-08-10
venue: 'arXiv preprint arXiv:2608.12345'
paperurl: 'https://arxiv.org/'
citation: '<b>Hannan</b>, Alex Taylor. (2026). &quot;Scalable Fault-Tolerant Distributed Memory Architectures for AI Clusters.&quot; <i>arXiv preprint arXiv:2608.12345</i>.'
---

### Abstract
As distributed training clusters scale to tens of thousands of accelerators, hardware failures become an inevitable daily occurrence. This preprint investigates zero-overhead asynchronous memory checkpointing coupled with RDMA-assisted state restoration to ensure uninterrupted continuous model training.

### Highlights
- Seamless memory snapshotting with sub-millisecond overhead.
- Rapid worker recovery using non-blocking RDMA ring topology.
- Tested across synthetic memory failure injection scenarios.

```bibtex
@article{hannan2026faulttolerant,
  title={Scalable Fault-Tolerant Distributed Memory Architectures for AI Clusters},
  author={Hannan and Taylor, Alex},
  journal={arXiv preprint arXiv:2608.12345},
  year={2026}
}
```
