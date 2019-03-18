---
title: Using human genetics to determine the direction of causality in a microbiome study 
post_snippet: “Typically microbiome studies can only claim to detect associations … in this case the authors use “Mendelian Randomization”, which theoretically can determine whether a given association is causal.”
---

[Sanna et al. 2019. Causal relationships among the gut microbiome, short-chain fatty acids and metabolic diseases. Nature Genetics.](https://www.nature.com/articles/s41588-019-0350-x) 

This is a summary of our DalMUG journal club discussion of this paper written by [Gavin Douglas](www.gavindouglas.ca).

### Summary

This paper focused on determining the links between human genetic variants, gut microbiota, and fecal short-chain fatty acid (SCFA) levels.
Typically microbiome studies can only claim to detect associations between features or disease states of interest when studying human
cohorts. However, in this case the authors used “Mendelian Randomization” (https://en.wikipedia.org/wiki/Mendelian_randomization), which
theoretically can determine whether a given association is _causal_. This technique confused us and we haven’t entirely wrapped our heads
around it so take the following explanation with a grain of salt. The key assumption of the approach is that genetic variants are
distributed randomly in a given population. If this is true then confounding factors affecting a disease or clinical phenotype should be
randomized in respect to genotype. An association between the genetic propensity for having a given exposure (e.g. such as the presence of
a particular gut bacterial species) and a phenotype of interest can then be tested. If there is an association than it has been argued
that this is causal since again other confounding factors should be distributed randomly across individuals and the focus is on the
genetic propensity of an exposure rather than the exposure itself. Although it was interesting to learn about this technique we weren’t
convinced that the key assumption mentioned above is reasonable. Nonetheless, we agree that the authors do show that the gut microbiome is _more
likely_ to be causally affecting clinical phenotypes by using Mendelian Randomization compared to standard microbiome data analysis.

### Points of Interest

* This was our first introduction to “Mendelian Randomization”! This is an example of tipping our toes into a scientific area with a huge body of literature and existing controversies. It’s difficult to know what the consensus is on whether it’s appropriate to state that associations identified by this approach are causal based on this paper alone.

* Interesting to see that P-value cut-off chosen for GWAS of LL-DEEP variants and microbial features was based on how genetic variance explained in independent cohort at different P-value cut-offs.

* As mentioned above, this method does suggest that the microbiome production of butyrate could be playing a direct role in improving insulin responses, which you wouldn’t be able to tell based on typical analyses

* Interesting to see that “Bracken” - which improves upon kraken/kraken2 output data - was used for taxonomic data. This will be an interesting tool to try out.


### Points of Confusion

* It wasn’t clear to us how different the main results have been if human genetics weren’t included? Would the GABA-degradation pathway (i.e. butyrate production) be the top hit?

* The main assumption of Mendelian Randomization is that genetic variants are distributed randomly across confounding factors. Currently the reader has no idea whether this is true or not in this cohort. It would have been useful to actually compare how confounding factors varied across the cohort to be more convincing.

* More generally, a major limitation of Mendelian Randomization is that links between genetic variants and exposures need to reliable. It wasn’t clear to us how the authors could be certain that the GWAS they performed was finding direct links between genetic variants and microbial features.
