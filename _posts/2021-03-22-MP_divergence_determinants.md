---
layout: post
title:  "Snapshot of our study: Elements and evolutionary determinants of genomic divergence between paired primary and metastatic tumors"
author: ruping
categories: [ clonal dynamics, mathematical modeling, detection bias ]
image: "https://raw.githubusercontent.com/ruping/figure/master/img/met_timing_graphical_abstract.png"
featured: true
rating: 5
---

We know that time is precious and below we give a short description of our recently published paper [“Elements and evolutionary determinants of genomic divergence between paired primary and metastatic tumors”](https://doi.org/10.1371/journal.pcbi.1008838).

Longitudinal tumor sampling provided us with the opportunity to quantify the between-tumor (stage) genomic divergence. However, it still remains a challenge about how to translate the genomic divergence between paired metastatic and primary tumor samples (M-P divergence) into the natural history of metastatic spread. Given a phylogenetic tree of these tumor samples constructed from NGS data, should we read a small M-P divergence as a sign of "early" metastatic seeding, or evidence of a "late" acquisiton of the metastatic potential? Before answering this clinically relevant question, one needs to characterize what exactly is being captured on the trees of tumor evolution by such divergence.

![Figure1](https://raw.githubusercontent.com/ruping/figure/master/img/20210322112926.png)

We show that the number of somatic variants of the metastatic seeding cell that are undetectable in the primary tumor sequencing data, i.e., the number of somatic variants specific to the metastatic seeding cell $B_{md}$, can be characterized as the path of the phylogenetic tree from the last appearing variant of the seeding cell back to <mark>the most recent detectable variant</mark>. In other words, the depth of the <mark>recent detectable variant</mark> in the seeding cell's geneaology characterizes the M-P divergence. The same reasoning applys to the number of somatic variants specific to the primary tumor $B_p$.

![Figure2](https://raw.githubusercontent.com/ruping/figure/master/img/20210322113007.png)

We find that the expected length of this path is principally determined by the decay in detectability of the variants along the seeding cell’s lineage; and thus, exhibits a significant dependence on the underlying tumor growth dynamics.

Let $c$ be a seeding cell of a secondary tumor (as opposed to the primary tumor) and also let
\begin{equation}
C = (c_0, c_1, . . . , c_{k_{seed}})
\end{equation}
be its associated set of variants, indexed according to the order of appearance as the primary tumor expands. Let $d_{c_j}$ denote the probability variant $c_j$ ends up being detectable in the primary tumor. We found that under the infinite allele model, the probability that $B_m^k$, the number of variants specific to the metastatic seeding cell (with $k$ somatic variants in total) take value $i$ can be expressed in a surprisingly simple form in terms of $d_{c_j}$:

<span class="spoiler">
\begin{equation}
Pr[B_m^k = i] = d_{c_{k-i}} - d_{c_{k-i+1}}.
\end{equation}
</span>

Despite the accumulation of somatic variants in the seeding cell as the primary tumor expands, dissemination from late detectable subclone leads to an abrupt drop in M-P divergence.

![Figure3](https://raw.githubusercontent.com/ruping/figure/master/img/20210322114635.png)





<!--
As with the last post about the editor, you'll want to be actually editing this post as you read it so that you can see all the Markdown code we're using.


## Special formatting

As well as bold and italics, you can also use some other special formatting in Markdown when the need arises, for example:

+ ~~strike through~~
+ ==highlight==
+ \*escaped characters\*


## Writing code blocks

There are two types of code elements which can be inserted in Markdown, the first is inline, and the other is block. Inline code is formatted by wrapping any word or words in back-ticks, `like this`. Larger snippets of code can be displayed across multiple lines using triple back ticks:

```
.my-link {
    text-decoration: underline;
}
```

#### JS

```js
// alertbar later
$(document).scroll(function () {
    var y = $(this).scrollTop();
    if (y > 280) {
        $('.alertbar').fadeIn();
    } else {
        $('.alertbar').fadeOut();
    }
});
```

#### Python

```python
print("Hello World")
```

#### Ruby

```ruby
require 'redcarpet'
markdown = Redcarpet.new("Hello World!")
puts markdown.to_html
```

#### C

```c
printf("Hello World");
```


![walking]({{ site.baseurl }}/assets/images/8.jpg)

## Reference lists

The quick brown jumped over the lazy.

Another way to insert links in markdown is using reference lists. You might want to use this style of linking to cite reference material in a Wikipedia-style. All of the links are listed at the end of the document, so you can maintain full separation between content and its source or reference.

## Full HTML

Perhaps the best part of Markdown is that you're never limited to just Markdown. You can write HTML directly in the Markdown editor and it will just work as HTML usually does. No limits! Here's a standard YouTube embed code as an example:

<p><iframe style="width:100%;" height="315" src="https://www.youtube.com/embed/Cniqsc9QfDo?rel=0&amp;showinfo=0" frameborder="0" allowfullscreen></iframe></p>

-->