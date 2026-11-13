# Part 0: The transformer as a candidate canonical cortical microcircuit

Yash Shah  
Nov 13, 2026

*Recently, myself and Daniel Yamins put out a preprint titled [The transformer as a candidate canonical cortical microcircuit](https://www.biorxiv.org/content/10.64898/2026.11.01.763457v1). You might find several interesting kinds of empirical analyses we performed to present the [transformer architecture](https://arxiv.org/abs/1706.03762) as a compelling candidate for the brain's [canonical cortical microcircuit](https://www.annualreviews.org/content/journals/10.1146/annurev.neuro.27.070203.144152)! To help break it down for quicker digestion, <u>I'm starting a series of blog posts that I will release at a weekly cadence</u>. Let me know your thoughts as you read through them :)*

---

Over the past decade, deep neural networks have become powerful tools for modeling various sensorimotor and cognitive regions of the brain such as [vision](https://www.pnas.org/doi/10.1073/pnas.2014196118), [language](https://www.pnas.org/doi/full/10.1073/pnas.2105646118), [audition](https://www.sciencedirect.com/science/article/pii/S0896627318302502?via%3Dihub), [motor control](https://www.nature.com/articles/nn.4042), [somatosensation](https://proceedings.neurips.cc/paper_files/paper/2025/file/639fa41231488ce73d8c4d6bb2886e81-Paper-Conference.pdf) etc.

Within vision neuroscience, convolutional neural networks (CNNs), in particular, have served as [de-facto models of the visual system](https://arxiv.org/abs/2001.07092). Their strong inductive biases of hierarchical organization and locality resemble several well-established properties of visual cortex.

Then, in 2017, came the transformer.

Originally developed for language, transformers have become a dominant architecture across artificial intelligence, including [computer vision](https://arxiv.org/abs/2010.11929). Like CNNs, transformers retain a hierarchical architecture. Unlike CNNs, transformers relax the locality constraint and use learned multiplicative interactions to dynamically integrate information across different parts of an input.

Could this (back then new) microcircuit extend the kinds of brain computations captured by CNNs?

**In this series, we (metaphorically) cut open the putative black box architecture of the transformer and analyze interactions between model units at the unit, population, and systems level and how they correspond to interactions at similar scales in the brain.**


## Convergent evolution between natural and artificial intelligence

[**Part 1 — Are transformers that different from convolutional networks?**](part1.md)

**Part 2 — Capturing computational mechanisms at the local circuit level**

**Part 3 — The issue of extraneous "brain-unlike" dimensions in models and how to deal with them**

**Part 4 — Simultaneously achieving high task performance and building wiring efficient systems**

**Part 5 — It is all about the multiplications!**


I hope this is intellectually stimulating!


---
Reach me by  
email: ynshah [at] stanford [dot] edu  
bluesky: @ynshah.bsky.social  
linkedin: @ynshah3  
x: @itsysxx