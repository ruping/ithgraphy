---
layout: post
title:  "How does the decay in detectability shape the between tumor genomic divergence"
author: ruping
categories: [ modeling, detection bias ]
image: "https://raw.githubusercontent.com/ruping/figure/master/img/img_0107.jpg"
featured: true
hidden: true
---
Hand drawing from [Athanasios N. Nikolakopoulos](https://www.nikolako.net/)

Let $c$ be a metastatic seeding cell (or the founder of a relapsed tumor) and also let
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