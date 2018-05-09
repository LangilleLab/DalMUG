---
title: Metabolic redundancy conferred by extrachromosomal replicons 
post_snippet: ...the replicons confer a substantial amount of redundancy in essential genes found in the genome. They also highlight insights that would not have been possible without also performing in silico metabolic reconstruction.
published: true
---

[diCenzo et al. 2018. Robustness encoded across essential and accessory replicons of the ecologically versatile bacterium Sinorhizobium meliloti. PLoS Genetics.](http://journals.plos.org/plosgenetics/article?id=10.1371/journal.pgen.1007357)

_This is a summary of our DalMUG journal club discussion of the above paper (when it was online as an uncorrected proof) written by **Gavin Douglas**._

### Summary
Several papers have recently demonstrated that knocking out the same gene within different strains of a species 
(and different species in a genus) can have drastically different fitness consequences. These observations have 
highlighted that the genomic background in which a gene is expressed partially determines whether a gene is essential 
or not. However, it’s still unclear how large-scale shifts in the genomic background, such as through gain of a plasmid, 
affects gene essentiality. Enter: di Cenzo _et al._ who investigated how the ancient acquirement of replicons (large plasmids) 
in the common soil bacteria _Sinorhizobium meliloti_ affected gene essentiality. These two replicons, pSymA and pSymA, encode 
~45% of the species’ genes. There are only 2 known essential genes on pSymB and otherwise the replicon-encoded genes are thought 
to be non-essential. The authors used Tn-seq to identify essential and growth-promoting genes while changing two variables: 
(1) whether the replicons are present or not and (2) whether the bacteria were grown in rich or defined media. They found that 
the replicons confer a substantial amount of redundancy in essential genes found in the genome. They also highlight insights that 
would not have been possible without also performing _in silico_ metabolic reconstruction.

### Points of Interest
* Interesting to know background on the relatively low percentages of essential genes that overlap across species/strains
* They created a transposon with constitutive promoters on both ends of the construct  to avoid issues where non-essential genes downstream of an essential gene in an operon are falsely identified as essential
* Some bias of the transposon to insert in GC-rich regions
* Identified 307 genes as essential independent of growth medium / strain
* Tested 4 genes predicted to produce no growth and they all agreed with the Tn-seq data, which was one example of a number of reassuring sanity checks
* Interesting that some fitness benefits of losing replicons could be due to having less DNA to synthesize
* Compared their results to _Rhizobium leguminosarum_, for which there is also a published Tn-seq dataset and found little overlap in their results overall
* Based on _in silico_ double KOs of a gene from chromosome and a gene from replicons they found 14% of chromosomal genes had predicted negative phenotype, which indicates high metabolic redundancy between chromosome and replicons
* 1/3 of reactions in reconstructed core metabolism were identified as not having an effect on growth based on Tn-seq
* They used the uncharacterized essential genes identified through Tn-seq to propose which genes were responsible for the predicted reactions (of unknown enzymes) in their reconstruction of core metabolism

### Points of Confusion
* The authors acknowledge that there could be problems with the constitutive promoters on the transposons, but it would be good to know what kind of off-target effects this would be expected to have
* Gene essentiality index looks like it is just (# insertions / gene length) - maybe including the possible number of insertion sites per gene would improve this measure?
* Of course in different environments (besides the two studied here) the replicons could become more or less important (which is really hard to assess)
* Would have been nice to compare the individual KOs of each replicons, especially since they have such different evolutionary histories
