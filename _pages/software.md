---
layout: archive
title: "Software"
permalink: /software/
author_profile: true
classes: software-page
---

[Hongying Li](https://stat.osu.edu/people/li.14067),
[Li Li](https://scholar.google.com/citations?user=UqZoDRcAAAAJ&hl=en), and I
jointly develop and maintain the <code>targetree</code> package, which is available in
[Python](https://github.com/Bill-Wang-Metrics/targetree-python),
[R](https://github.com/Bill-Wang-Metrics/targetree-r), and
[Stata](https://github.com/Bill-Wang-Metrics/targetree-stata).

<code>targetree</code> helps empirical researchers construct, evaluate, and
visualize interpretable binary classification trees for policy targeting. The
three implementations provide a common workflow for fitting CART, PFS, and
MDFS trees and presenting the resulting targeting policies.

## What targetree produces

The figure below illustrates the package's main output: an interpretable
targeting policy constructed from a fitted classification tree. At each
internal node, the left branch satisfies the displayed condition and the right
branch does not. Each terminal node reports the subgroup's estimated outcome
probability, $\hat{\mu}$, and sample size, $N$. Blue terminal nodes are targeted
because their estimated probabilities exceed the policy threshold of 0.35;
white terminal nodes are not targeted.

<figure class="targetree-example">
  <a href="{{ '/files/targetree-mdfs-tree.pdf' | relative_url }}" aria-label="Open the targeting-policy diagram as a PDF">
    <img src="{{ '/images/targetree-mdfs-tree.png' | relative_url }}" alt="MDFS targeting policy shown as a binary tree. Internal nodes contain split rules, and blue terminal nodes identify subgroups with estimated outcome probabilities above 0.35.">
  </a>
  <figcaption>
    Example targeting policy constructed using MDFS. Select the figure to open
    the full-resolution PDF.
  </figcaption>
</figure>
