---
title: Meta-analysis of metagenomics-identified KEGG profiles across multiple diseases
post_snippet: ...Armour et al. analyzed over 2000 metagenomics samples from 8 studies, which represented a range of diseases… since this is a pre-print hopefully the feedback below is helpful!
---

[Armour et al. 2018. A Metagenomic Meta-Analysis Reveals Functional Signatures of Health and Disease in the Human Gut Microbiome. bioRxiv.
](https://www.biorxiv.org/content/early/2018/03/23/286419)

_This is a summary of our DalMUG journal club discussion of this paper written by **[Gavin Douglas](http://www.gavindouglas.ca/)**_

### Summary
This pre-print was motivated by two trends:

(1) Microbiome studies normally focus on single diseases and
(2) Most meta-analyses of microbiome studies have focused on taxa

To address these limitations, Armour et al. analyzed over 2000 metagenomics samples from 8 studies, which represented a range of diseases. Our journal club enjoyed reading this pre-print since we believe more meta-analyses are needed in this area. There were a number of sections that we believe could be clarified or could benefit from further analyses; since this is a pre-print hopefully the feedback below is helpful!

### Points of Interest
* Weak association between functional richness and Bray-Curtis dissimilarity with disease states overall
* 484/521 KEGG modules are associated with at least one disease and many of these are associated with multiple diseases
* Nice to see quantification of how study effect (at least in case of obesity) is much more important that disease state for explaining functional profiles
* Testing the “Anna Karenina principle” was interesting to read about - **more studies should test this idea!**


### Points of Confusion
* We were a little confused about the different counts reported for the runs and samples given how the authors later specify only a single run was used per sample - this would be worth clarifying further
* Unclear whether human DNA was removed from FASTQs as part of MetaQuery pipeline - it would be helpful to explain in one sentence what the reference mapping step of that pipeline does.
* Unclear how differences in sequencing depth across studies and samples was controlled for - this seems especially important when comparing functional richness
* Similarly, it would have been interesting to see tests of several metrics of functional alpha-diversity - not just richness, which may be driven entirely by differences in taxonomic richness
* Unclear why such a lenient FDR cut-off (0.2) was used; were the authors originally expecting very few significant KEGG modules? Related to this point it was not always clear how the highlighted modules that were discussed in main-text were chosen given that so many modules were significant.
* Presenting Table 2 as a heatmap (e.g. just by colouring the cells by magnitude in excel) might make the similarities between diseases easier to see.
* Very interesting to see quantified study effect, but would it be possible to break this effect down further by sequencing tech., cohort age range, etc.?
* Figure 4 is not mentioned in the main-text
