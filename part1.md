# Part 1: Are transformers that different from convolutional networks?

Yash Shah  
Nov 13, 2026

In [Part 0](part0.md), I introduced the transformer as a candidate model of cortical computation. Transformers are often thought to be poor models of cortical computation because of their putatively global attention mechanism, which allows every unit in a layer to interact with every other unit. But this view misses an important point: transformers share many computational principles with both CNNs and the brain.

## Transformers extend, rather than replace, CNNs

The transformer largely builds on the same computations as CNNs. The primate visual system is organized [retinotopically](https://physoc.onlinelibrary.wiley.com/doi/10.1113/jphysiol.1962.sp006837) and [hierarchically](https://www.nature.com/articles/nn1100_1199). CNNs and transformers share this organization: both process visual information through successive layers, with neighboring units responding to neighboring parts of the visual field.

The key difference lies in the transformer's attention module. Attention allows the activity of one unit to multiplicatively modulate the activity of another, providing a way to dynamically route information between different parts of an image.

**The key difference is not simply that CNNs are local and transformers are global. Transformers extend CNN computations by allowing distant units to interact through learned multiplicative operations.**

There are biological analogues of these interactions: [context-dependent gain modulation](https://www.sciencedirect.com/science/article/pii/S0896627300000040) and [long-range lateral interactions](https://www.pnas.org/doi/abs/10.1073/pnas.90.22.10469) are both well-documented features of mammalian cortex.

<img src="figures/part1/fig1.png" width="100%">

Given their ability to integrate information across distant image regions, we might expect transformers to develop very different representations from CNNs.

CNNs have an explicit bias toward locality. Early layers process small image regions; deeper layers progressively integrate information over larger areas. Standard transformers have no such restriction: attention can connect distant image regions from the very first layer.

But do these differences in single-unit computations actually lead to different population-level organization?

## Long-range lateral connections in transformers are sparse

Visualizing learned attention matrices reveals that **units do not connect uniformly to every other unit in a layer**. Most interactions are local, regardless of where a layer sits in the model hierarchy. Only a smaller fraction span longer distances.

<img src="figures/part1/fig2.png" width="35%">

## Transformers learn spatially local receptive fields

In the primate visual system, successive stages of the visual hierarchy integrate information over increasingly large regions of visual space, creating a [progression from local to global representations](https://www.cell.com/current-biology/references/S0960-9822(14)01653-4).

CNNs develop this hierarchy naturally through architectural parameters such as kernel size, stride, and pooling. Transformers, by contrast, have access to global interactions at every layer.

Yet **when trained on natural images, transformers develop the same local-to-global receptive field hierarchy.**

This is striking: since transformers have sparse global connections and most connections between units are local within each layer, transformers learn to organize their computations spatially.

<img src="figures/part1/fig3.png" width="50%">

## What does this tell us?

Transformers are not as different from CNNs as their architectures might suggest. Like CNNs, they develop **hierarchical, retinotopic representations with a local-to-global receptive field structure**. They also retain a sparse set of longer-range lateral interactions.

So what do these multiplicative operations and long-range interactions actually contribute? And what can they explain about the brain that CNNs cannot?

Stay tuned!

---

Reach me by  
email: ynshah [at] stanford [dot] edu  
bluesky: @ynshah.bsky.social  
linkedin: @ynshah3  
x: @itsysxx