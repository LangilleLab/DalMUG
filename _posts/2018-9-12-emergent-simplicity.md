---
title: Mice undergoing experimental colitis have distinct bacteriophage populations
post_snippet: Altered viral populations have been observed in adults with IBD, but there has yet to be controlled experiments of phage dynamics in experimental mice models of IBD. In this study, Duerkop et al. find differences in bacteriophage after induction of colitis in mice. 
---

[Duerkop et al., 2018. Murine colitis reveals a disease-associated bacteriophage community. Nature Microbiology.](https://www.nature.com/articles/s41564-018-0210-y)

_This is a summary of our DalMUG journal club discussion of this paper written by **[Casey Jones](https://twitter.com/CaseyMAJones)**_

### Summary
The dynamics of bacteriophage in inflammatory bowel diseases (IBD) in the gut aren’t as well understood as that of bacteria, yet there is [estimated](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3975094/) to be nearly as many phage as there are bacteria in the gut. Phage may play a role in gut homeostasis by modifying bacterial populations or by [providing protection](https://www.ncbi.nlm.nih.gov/pubmed/23690590/) of the gut mucosa. Altered viral populations have been observed in [adults with IBD](https://www.ncbi.nlm.nih.gov/pubmed/25619688), but there has yet to be controlled experiments of phage dynamics in experimental mice models. 

In this study, Breck Duerkop and colleagues attempt to define the gut virus community in a mouse model of T-cell mediated colitis. They sequence both whole metagenome and virus-like particle (VLP) enriched samples in colitic mice and saline-injected controls. To define viral communities in the gut, they curated their own virome database of 1104 contigs based on their presence in the VLP samples compared to controls. 

Through inference of bacterial composition by 16S rRNA gene reconstruction using [phyloFlash](https://github.com/HRGV/phyloFlash), they found an increased abundance of Proteobacteria at 42 days post-Colitis induction, coinciding with increased levels of phage infecting certain Proteobacteria genera. They also found considerable overlap between the phage contigs from mice and adult patients with IBD from a [previous study](https://www.ncbi.nlm.nih.gov/pubmed/25619688). 

We were pleased with the findings of the study, but had some concerns as outlined below. Overall it seems that mouse models may be useful for studying the virome of IBD. 


### Points of Interest
* Mapping whole metagenome reads to virally-enriched reads is a novel way of defining presence of viruses and merits further validation 
* The overlap of human and murine contigs substantiates the use of murine models to study IBD 


### Points of Confusion
* Having only three mice in each treatment group may not have sufficient power
* How many VLP reads were thrown out from mapping to contigs from germ-free mice? 
* Why not use [Kraken](https://ccb.jhu.edu/software/kraken/) instead of phyloFlash (16S inference) approach?
* We found the use of a one-way analysis of variance in Figure 1c not overly statistically convincing. 
* How was a “core” virome defined? 
* Why were Microviridae genomes from NCBI not used in addition to the Caudovirales? These non-tailed phage were [recently shown](https://www.ncbi.nlm.nih.gov/pubmed/30169455) to be lower in abundance in Crohn’s Disease patients versus controls.
