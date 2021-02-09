---
layout: post
title:  "Does a RNA-seq experiment reach saturation?"
author: ruping
categories: [ RNA-Seq ]
tags: [red, yellow]
image: "https://raw.githubusercontent.com/ruping/figure/master/img/pos_tag.png"
description: "Fractional Coverage versus Depth of Coverage"
featured: false
---

The term "coverage" for a gene in an RNA-seq experiment can be viewed in two ways. The first is the overall number of reads (<mark>depth of coverage</mark>) that are mapped to the gene, which serves to deduce a normalized "transcriptional abundance" measurement, such as the widely used `R(F)PKM` (Reads or Fragments Per Kilobase of transcript per Million reads mapped) and `TPM` (Transcripts Per Million). See a recent [paper](https://rnajournal.cshlp.org/content/early/2020/04/13/rna.074922.120) for these. However, less mentioned the other the fraction of the gene covered, more strictly, the positions in the gene where a tag starts from (<mark>fractional coverage</mark>). Plotting these two "coverage"s for each gene is an effective way to highlight an RNA-seq experiment's quality. The rationale behind such a plot is that if the depth of coverage is high, the gene should presumably reach a high fractional coverage. If the fractional coverage remains low for very high depth of coverage, the experiment may have strong position bias which suggests a suboptimal sampling of the RNA molecules. 

<!--
#### How to use?

It's actually really simple! Add the rating in your YAML front matter. It also supports halfs:

```html
---
layout: post
title:  "Inception Movie"
author: john
categories: [ Jekyll, tutorial ]
tags: [red, yellow]
image: assets/images/11.jpg
description: "My review of Inception movie. Actors, directing and more."
rating: 4.5
---
```
-->
