--- 

title: Investigating the proportion of pangenome variance explained by phylogenetic inertia and the environment
post_snippet:  ... used correlation-adjusted regression to determine the percentage of variance in each pangenome feature … overall the species’ environments explained a larger proportion of variance ...
published: true
--- 

[Maistrenko et al. Disentangling the impact of environmental and phylogenetic constraints on prokaryotic within-species diversity. The ISME Journal](https://www.nature.com/articles/s41396-020-0600-z)

_This is a summary of our Dalhousie Microbiome User Group (DalMUG) journal club discussion of this paper written by [Gavin Douglas](http://www.gavindouglas.ca)._

### Summary
Prokaryotic species pangenomes can be characterized by a range of metrics, such as core genome size, total genome size, and inter-strain distance. These metrics can substantially differ across species for many possible reasons. Two broad factors are phylogenetic inertia (the evolutionary history of a given species) and environmental influences. Maistrenko et al. investigated the relative contribution of these factors by investigating ~7000 genomes representing 155 species. To do so, they annotated the genomes, computed 21 key pangenome features, and identified the likely habitats of each genome. They used correlation-adjusted regression to determine the percentage of variance in each pangenome feature that could be explained by the species’ phylogenetic inertia and environment. Although there was variation across features overall the species’ environments explained a larger proportion of variance relative to phylogenetic inertia. In addition, most of the variance could be explained by a combination of these factors for features associated with pangenome size. In contrast, the variance in features representing intra-species pangenome diversity (such as genome fluidity) was largely unexplained by the investigated factors.


### Points of Interest

* A range of methods (including mapping 16S sequences to a database with 16S-habitat associations) were used to identify potential genome habitats. Initially we were skeptical of how well these methods might work, but we realized that any noise added by these methods should make their conclusions more conservative

* Genome fluidity and pangenome saturation were not significantly correlated, which was especially interesting because both measures are commonly used to measure pangenome openness and are often used interchangably

* Very interesting that the nucleotide diversity best explained the functional distance metric: this is consistent with recent findings that effective population size are positively correlated with pangenome diversity

* Interesting that normalized core genome size was associated with species habitat ubiquity while inter-strain functional distance was not. We definitely expected beforehand that habitat ubiquity would be more so associated with functional distance.

* Interesting to see the validation of their main result with larger genome sets. It was clever to just focus on genome size as a proxy for other pangenome features (which allowed the authors to leverage data from species where only a few genomes were available)

* Interesting to see that core genome size and other traits show evidence of convergent evolution across independent prokaryotic lineages


### Points of Confusion

* The authors used the first 5 phylogenetic PCs (80% of variance) and first ten habitat PCs (50% of variance) in their models - why not use a number of PCs that explained a more similar level of variance between the two data types?

* The correlation-adjusted regression approach for decorrelating variables seems really powerful, but we were curious what caveats this approach might have. It would have been nice to have this discussed

* The environments / habitats accounted for in this study were quite coarse (such as being found in a lake or ocean). We wondered how much more variance might be explained if data were available on micro-niches, which might be more relevant to small differences in genome content
