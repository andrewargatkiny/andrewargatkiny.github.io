---
layout: about
title: about
permalink: /

profile:
  align: right
  image: profile_pic.jpg
  image_circular: false # crops the image to make it circular

news: false # includes a list of news items
selected_papers: false # includes a list of papers marked as "selected={true}"
social: true # includes social icons at the bottom of the page
---

I’m an ML research scientist with a mission to make the neural network architectures, which power modern Large Language Models, computationally efficient and, at the same time, scalable linearly w.r.t. sequence length, which would eliminate the major bottleneck of current standard architectures. Hopefully, it may expedite the path to AGI by dramatically reducing compute requirements for prolonged chains-of-thought like in OpenAI's o1 models and their future counterparts. 

Previously I worked as a machine learning engineer in the industry where I built, shipped and oversaw high-load end-to-end ML pipelines impacting tens of millions daily users across diverse business domains.

I'm the author of [DenseAttention Network](https://github.com/andrewargatkiny/dense-attention) – a simplification of standard Transformer architecture which can serve as its drop-in replacement. It has several favorable properties:

1. The architecture can run in both $$O(N)$$ and $$O(N^2)$$ time and space w.r.t sequence length $$N$$ depending on which option is optimal. 
2. Despite being implemented in pure Pytorch, it's *significally faster*  than standard architecture in both regimes. For small sequences, the gain in speed in $$O(N^2)$$ regime **is up to 77.1%**, as compared to default Transformer implementation, and it's **up to 15%** faster than low-level FlashAttention-2 implementation. And for long sequences, the model in $$O(N)$$ regime is faster by **orders of magnitude**.
3. The model **achieves SOTA** on Long Range Arena (LRA) benhmark by a large margin among  all Transformer-based or inspired models and even **competes** with State-Space-Model architectures, such as S4.
4. The BERT-like architecture with DenseAttention Network blocks instead of Transformer ones demonstrates quality **on par or better** than the original.
5. And the last, the model is very *conceptually simple* and closely resembling the standard Transformer which makes it suitable for widespread adoption among practitioners' community.
