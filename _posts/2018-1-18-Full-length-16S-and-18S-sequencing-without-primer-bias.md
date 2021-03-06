---
published: true
post_snippet: ...an optimized method to sequence full-length small subunit ribosomal RNA by combining novel sequencing and molecular tagging protocols.
title: Full-length 16S and 18S sequencing without primer bias
---

#### [Karst et al. 2018. Retrieval of a million high-quality, full-length microbial 16S and 18S rRNA gene sequences without primer bias. Nature Biotechnology.](https://www.nature.com/articles/nbt.4045)

_Summary of DalMUG group discussion written by:
**Akhilesh Dhanani**_

### Summary

Recent technological advancement in high-throughput DNA sequencing has greatly improved our knowledge of hidden variation in microbial communities from microbial ecology studies. However, most studies to date rely on sequencing of short fragments of the 16S/18S rRNA gene using “universal” primers which often fails to distinguish closely related microbial taxa and may miss some clades altogether. In this paper, Karst et al. present an optimized method to sequence full-length small subunit ribosomal RNA (SSU rRNA) by combining novel sequencing and molecular tagging protocols. Briefly, enriched SSU rRNA was used to generate double-stranded cDNA by poly(A) tailing to avoid the use of traditional universal primer and subsequent taxonomic bias. Each RNA molecule was uniquely tagged so that reconstruction of full-length SSU rRNA sequence by de novo assembly could be achieved at the end. 

The authors applied their method to seven complex ecosystems and generated more than 1 million SSU rRNA sequences across all domains of life. To demonstrate that their method enabled novel SSU rRNA sequences to be identified, they compared the sequences obtained from the use of traditional full-length universal primers with their primer-free approach. Interestingly, they found a large proportion of novel diversity especially in the archaeal (mainly Asgard Archaea) and bacterial domains. 

Overall, this paper presents an interesting approach to expand current reference databases and our knowledge of microbial diversity.

### Points of Interest

* Their methodology used to generate SSU rRNA sequences is well explained. All steps for molecular conversions are supplemented with reagents and quantity used. This information is critical for other labs to reproduce their approach. Their use of several independent validations also makes us confident in their method.

* Primer-based sequencing approaches are limited in their application to identify novel sequences from extreme and diverse environmental samples. This primer free novel approach generated one million SSU rRNA sequences from seven diverse ecosystems. Out of 44,902 bacterial OTUs clustered at 97% similarity, 58% full-length OTUs present novel diversity when compared to the SILVA database. 

* Identification of novel lineages in recently defined Patescibacteria/Candidate Phyla Radiation (CPR) and the Asgard Archaea superphylum. 

* It has long been believed that primer bias leads to “missing diversity” in all microbiome studies. Validation of “missing diversity” with different primers ranged between 8.5 – 14.7% when compared to full-length SSU rRNA sequences.

### Points of Confusion

* Conclusion of lower error and chimera rate was based on mock community made up of just three individual microbes. It may have been interesting to use a complex mock community.

* Although this method is able to capture novel diversity it likely has several drawbacks compared to primer-based approaches. For instance, RNA is prone to degradation and differentially expressed under varying conditions, and thus may not give a true quantitative representation of microbial diversity. In addition, this library preparation would have much higher cost compared to traditional primar-based methods.

* Again, the number of molecular conversions in their methods to generate stable cDNA from total RNA is not an efficient process and also leads to the loss of true community representation.

* A MiSeq was used for both RNA and DNA based SSU rRNA sequencing. It was not explained why the authors chose to do paired-end 1x240bp and 1x25bp instead of simply using the traditional and possibly more insightful 2x300bp paired-end sequencing instead.

