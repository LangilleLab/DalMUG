---
published: true
title: Studying metabolic horizontal gene transfer through ancestral state reconstruction and flux balance analysis
post_snippet: ...how are complex traits, those dependent on a large number of genes, transferred by HGT?
---

#### [Pang and Lercher. 2019. Each of 3,323 metabolic innovations in the evolution of _E. coli_ arose through the horizontal transfer of a single DNA segment. PNAS USA](https://www.pnas.org/content/116/1/187)

_Summarized from DalMUG group discussion and written by: [**Gavin Douglas**](http://www.gavindouglas.ca/)_

### Summary
Bacteria are known to commonly exchange genetic material through horizontal gene transfer
(HGT; also known as lateral gene transfer) that enables them to adapt to novel environments.
These adaptations often involve a gain or shift in a metabolic trait (e.g. the ability to metabolize a different sugar).
There are many exciting questions in this area, but one pertinent one is how are complex traits, those dependent on a large number
of genes, transferred by HGT? There are three clear possibilities: complex traits are (1) transferred by single large events,
(2) by multiple non-complex neutral events, or (3) by stepwise non-complex events with incremental increases in fitness.
Pang and Lercher took a bioinformatics approach to investigate these possibilities across intestinal strains of _E. coli_.


### Points of Interest
- Clear description of the immense metabolic diversity across E. coli strains.

- Used GLOOME to infer the patterns of gene gain and loss across the strain lineages.

- Besides strains that are nearly identical, phenotypic similarity was independent of amino acid sequence divergence (which contrasts with the trend at longer timescales).

- Interesting way to compute all possible metabolic pathways - simply combine all of the networks together and compute a super-metabolic network.

- Based on the theoretically possible transfers - only 2.4% of new phenotypes and 7.4% of yield improvements required the acquisition of multiple DNA segments (i.e. bigger than 30kb separate).

- Of the 3,323 actual transfers inferred all involved genes within 30 kb of each other (even the <3% that required more than 5 relevant genes)

- Importantly 10-20% of new phenotypes required a pre-existing transfer event (i.e. an adaptive stepping stone, which is consistent with explanation #3 above).

### Points of Confusion

- Why restrict the analysis to ~50 strains when so many others are available?

- Are different mechanisms of HGT more or less compatible with the upper transfer limit of 30 kb?

- The italicized sentence from the paper below is very interesting, but we’re not totally sure how to interpret it - does it mean that intermediate transfers of a complex trait also always occurred in the same genomic region?

_Note that every single one of these apparently complex phenotypic innovations could instead have been bestowed on the immediate ancestor of the successive DNA acquisitions through a single <30-kb DNA segment presently found in one of the other extant _E. coli_ strains._

- A clearer breakdown of what the simulated environments consisted of would have been useful to better evaluate the methods.
