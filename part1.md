# Part 1: Are transformers that different from convolutional networks?

Yash Shah  
Nov 13, 2026

In [Part 0](part0.md), I claimed that convolutional networks (CNNs) have thus far served as de-facto models of the ventral visual system, but transformers as a newer model class might offer a better characterization of the brain's computation.

## You might expect transformers to be very different from CNNs

CNNs are built around locality. Early layers process small image patches, and deeper layers integrate over progressively larger regions. Transformers, on the other hand, do not have this strong locality bias. They are capable of forming global connections via the attention mechanism at every layer.

## But transformers are hierarchical, retinotopic, and mostly local, with receptive fields that grow across layers, just like CNNs

The primate visual system is organized [retinotopically](https://physoc.onlinelibrary.wiley.com/doi/10.1113/jphysiol.1962.sp006837) and [hierarchically](https://www.nature.com/articles/nn1100_1199), such that  successive stages integrate over increasingly large regions of visual space, forming a progression from local to global receptive fields.

CNNs are hierarchical as they stack linear--nonlinear layers one after the other. And they implement the progression of increasing receptive field sizes with model depth as a strong inductive bias through architectural parameters such as small kernel sizes, stride, and pooling.

<br>
<img src="figures/part1/fig1.png" width="100%">
<br><br>

However, **transformers are similarly hierarchical and, despite the potential for long-range connections, mostly local!**

<br>
<img src="figures/part1/fig2.png" width="50%">
<br><br>

A consequence of this *learned* locality is that **when they are trained on natural images, transformers *learn* the same progression as CNNs**: small receptive fields in early layers and larger ones in later layers.

<br>
<img src="figures/part1/fig3.png" width="70%">
<br>

## So are transformers different from CNNs at all?

Trained ViTs are mostly local, much less global than you’d think. But, they possess <u>sparse long-range connections</u>, which explain important brain motifs that I will tell you about in later weeks.


Stay tuned to find out!

<br><br>
---

Reach me by  
email: ynshah [at] stanford [dot] edu  
bluesky: @ynshah.bsky.social  
linkedin: @ynshah3  
x: @itsysxx