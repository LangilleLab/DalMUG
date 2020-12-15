---
title: PPanGGOLiN - A tool for graphically summarizing pangenome diversity
post_snippet:  ... difficult to visualize the overlap in strain genome contents when the number of genomes becomes large. PPanGGOLiN is a tool that addresses this problem...
published: true
---

[Gautreau et al. 2020. PPanGGOLiN: Depicting diversity via a partitioned pangenome graph. PLOS Computational Biology.](https://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1007732)

_This is a summary of our Dalhousie Microbiome User Group (DalMUG) journal club discussion of this paper written by [Gavin Douglas](http://www.gavindouglas.ca/)._

### Summary
One challenge in characterizing species pangenomes is that it becomes difficult to visualize the overlap in strain genome contents when the number of genomes becomes large. PPanGGOLiN is a tool that addresses this problem by building upon past consensus graph approaches to visualize gene content variation. In the PPanGGOLiN output graph each node is a gene and each edge is a relation of genetic contiguity (i.e. the genes are next to each other in the same genome). Genes are classified into different pangenome subsets based on fitting Bernoulli Mixture Models to the presence/absence matrix of genes across genomes. These partitions correspond to the persistent genome (i.e. what is commonly called the “soft core” genome), the shell genome (genes at intermediate frequency, which can be split into further partitions), and the cloud genome (rare genes). This is done in combination with a Markov Random Field to weight neighbouring genes as more likely to be in the same partition. The authors show that the resulting graph is useful from several perspectives, such as providing graph metrics that can be compared across partitions and species. They also made several useful biological observations in their own right by applying this tool to several genome datasets. We thought this was an interesting paper that seemed like it could be a valuable tool for the field.


### Points of Interest
* Great example of different possible paths for capsular polysaccharide synthesis in _Actinetobacter baumanii_
* Convincing that their approach works better than the “soft core” 95% cut-off approach for defining persistent genes
* The comparison in pangenomes between MAGs and reference genomes was also convincing that an approach like PPanGGOLiN is needed to make sense of cases where you have thousands of genomes to summarize


### Points of Confusion
* How would the results change if species were defined using a more consistent framework (like using average nucleotide identity for instance)?
* Why does the mu parameter differ across each Bernoulli mixture model? I think we must be missing regarding how each model is fit to each partition.
* It seemed circular to us that the distance between the shell and phylogenetic distances would be highly correlated with the proportion of the shell genome per genome.
* Given that the shell genomes of species differ so drastically depending on what MAGs / genomes are included, maybe different terminology should be used to emphasize what the genomes used were rather than to refer to the result as the “species” pangenome.
* There was some disagreement in our discussion about where the “soft core” cut-off might actually make for more standardized cross-species comparisons whereas comparing the proportion of shell/persistent genes based on PPanGGOLiN might be more difficult to interpret. 
