---
published: true
title: Mining for regulatory sequence gold in the genomes of prokaryotes
post_snippet: Johns et al., use a high throughput GFP reporting screen to test the regulatory features of over 29,000 unidirectional intergenic regions from 184 different prokaryotic genomes.
---

#### [Johns et al. 2018. Metagenomic mining of regulatory elements enables programmable species-selective gene expression. Nature Methods.](https://www.nature.com/articles/nmeth.4633)

_Summarized from DalMUG group discussion and written by:
**Jacob Nearing**_

### Summary

In this study Johns et al., use a high throughput GFP reporting screen to test the regulatory features of over 29,000 unidirectional intergenic regions from 184 different prokaryotic genomes. The group uses three different organisms, *Bacillus subtilis*, *Escherichia coli*, and *Pseudomonas aeruginosa*, to test expression levels using both RNA-seq and FACS-seq. Of these three organisms, *B. subtilis* was found to be the least capable of using regulatory sequences from other species whereas *P. aeruginosa* was the most capable of using these sequences. Furthermore they characterized several metrics such as GC content that could be used to predict if a regulatory sequence would be universally expressed by all three different species.
	
Looking at translation levels of different regulatory sequences showed that despite 16.9% of all regulatory sequences in the library showing active transcription, only 3.3% showed active translation. This highlights that the production of a transcript does not always lead to its translation. However, they did find a correlation between increased transcript levels and increased GFP expression. Interestingly, *P. aeruginosa* was capable of using only 9% of the actively transcribed regulatory sequences for translation, indicating a large barrier at the translation level. Both *E.coli* and *B. subtilis* translated 20-30% of regulatory sequences that actively allowed the transcription of the GFP mRNAs. Using this knowledge the group was also able to engineer plasmids with species specific expression patterns.
	
In conclusion this work has created vast amounts of valuable information on different regulatory sequences and their expression profiles across three different bacterial species. Furthermore, the authors produced metrics that could be used to find regulatory sequences that allow universal expression creating a strong starting point for many synthetic biological circuits. 

### Points of Interest
* It is interesting that *Pseudomonas aeruginosa* can use the most regulatory sequences, as it is known to be found in many diverse environments. 
* Although 16.6% of transcripts were universally transcribed, only 3.3% were translated. This shows how risky it may be to assume transcription means translation in some contexts.
* Provides a vast amount of information with high potential to create useful biological synthetic circuits in the future.
* Figure 3C - the regression models used 10% of the data to train and 90% of the data to test. Not a usual practice that is seen but does strengthen their conclusion. 

### Points of Confusion
* Does genome size/number of genes correlate with the amount of regulatory sequences an organism can utilize?
* We did not understand why all the Y-axis labels were different in Figure 3.
* Would have liked to see the false positive rate for the regulatory sequences that showed GFP expression but did not show transcript levels.

