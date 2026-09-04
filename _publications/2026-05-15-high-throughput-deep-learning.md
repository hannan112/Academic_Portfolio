---
title: "High-Throughput Compression-Accelerated Communication for Distributed Deep Learning"
collection: publications
category: conferences
permalink: /publication/2026-high-throughput-deep-learning
excerpt: 'We propose a lightweight, GPU-accelerated compression framework that reduces inter-node collective communication latency by up to 3.8x in large-scale model training.'
date: 2026-05-15
venue: 'IEEE/ACM International Conference on High Performance Computing, Networking, Storage and Analysis (SC &#39;26)'
paperurl: 'https://arxiv.org/'
slidesurl: 'https://github.com/'
citation: '<b>Hannan</b>, Jane Doe, John Smith. (2026). &quot;High-Throughput Compression-Accelerated Communication for Distributed Deep Learning.&quot; <i>SC &#39;26: Proceedings of the International Conference for High Performance Computing</i>.'
---

### Abstract
Distributed training of modern deep learning models is increasingly bottlenecked by inter-node communication bandwidth. In this work, we present a novel co-designed compression-communication framework tailored for GPU collectives. By interleaving adaptive lossy/lossless compression algorithms directly inside the communication kernel, we achieve significant latency reduction without degrading training convergence or model accuracy.

### Key Contributions
- **Hardware-Aware Compression:** Optimized CUDA kernels that exploit tensor core parallelism for ultra-fast encoding.
- **Dynamic Error-Bounding:** Adaptive quantization thresholds based on gradient distribution shifts across training epochs.
- **Extensive Benchmarking:** Evaluated on multi-node GPU clusters across LLaMA, Vision Transformers, and recommendation systems.

```bibtex
@inproceedings{hannan2026compression,
  title={High-Throughput Compression-Accelerated Communication for Distributed Deep Learning},
  author={Hannan and Doe, Jane and Smith, John},
  booktitle={SC '26: Proceedings of the International Conference for High Performance Computing, Networking, Storage and Analysis},
  year={2026}
}
```
