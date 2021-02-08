---
layout: post
title:  "The art between growth, seeding and detectability."
author: ruping
categories: [ modeling, detection bias ]
image: "https://raw.githubusercontent.com/ruping/figure/master/img/img_0107.jpg"
featured: true
hidden: true
---
Hand drawing from [Athanasios N. Nikolakopoulos](https://www.nikolako.net/)

Assuming that the primary tumor growth follows a multi-type branching process, the founder cell was the original type (type 0). A new type was born (type 1, which grows faster) as the tumor expands, which eventually reached a detectable fraction in the final tumor. Seeding from these two distinct cell groups would lead to distinct patterns in the resulting genomic divergence between the secondary tumor originated from the seeding cell and the primary tumor. The hand drawing above shows the transition between seeding from type 0 and from type 1 as the primary tumor expands. Let's further posit that the seeding potential is somehow related to the growth rate. The S-shape transition reflects the consideration that when enough of the type 1 are around, the next division will come from this new type, which will devastate the probability of seeding from the type-0 cells.

Let $c$ be a seeding cell of a secondary tumor (as opposed to the primary tumor) and also let
\begin{equation}
C = (c_0, c_1, . . . , c_{k_{seed}})
\end{equation}
be its associated set of variants, indexed according to the order of appearance as the primary tumor expands. Let $d_{c_j}$ denote the probability variant $c_j$ ends up being detectable in the primary tumor. In our [paper preprint](https://www.biorxiv.org/content/10.1101/2020.08.24.262378v1), we found that under the infinite allele model, the probability that $B_m^k$, the number of variants specific to the metastatic seeding cell (with $k$ somatic variants in total) take value $i$ can be expressed in a surprisingly simple form in terms of $d_{c_j}$:

<span class="spoiler">
\begin{equation}
Pr[B_m^k = i] = d_{c_{k-i}} - d_{c_{k-i+1}}.
\end{equation}
</span>

 


<!--
#### So how do we do spoilers?

```html
<span class="spoiler">My hidden paragraph here.</span>
```
-->