---
title: Group review of the preprint “Removal of rare amplicon sequence variants from 16S rRNA gene sequence surveys biases the interpretation of community structure data”

published: true
---

This post is a review of a recent bioRxiv preprint:
[Schloss 2020. Removal of rare amplicon sequence variants from 16S rRNA gene sequence surveys biases the interpretation of community structure data. bioRxiv.](https://www.biorxiv.org/content/10.1101/2020.12.11.422279v1)


This review was written by members of the Langille Lab (Dalhousie University) and was based on a journal club discussion.


### Overview

Pat Schloss investigated how filtering rare ASVs from 16S datasets affects several aspects of microbiome analysis, such as estimating alpha and beta diversity and the power to detect overall signals. He concluded that filtering rare ASVs has negative effects in general and in many cases the effect sizes are large.

From one perspective we applaud this preprint: we think more investigations into fundamental choices in microbiome data analysis should be made publicly available, as this work has done. However, we were unconvinced by the preprint’s arguments. The key issues we discussed were related to two problems:

**1. Insufficient detail on methods provided to fully evaluate all results**

**2. The focus on the null-generated samples resulted in analyses where the results seemed contrived and unlikely to be representative of real data**

Overall, we believe this research question deserves the merit/focus given to it. However, a more straightforward analysis based on using the actual treatment groups and actual community structures, and then showing that the conclusions reached for each would (or would not) change based upon the presence of the actual rare ASV distributions in those samples, would have been much more convincing.


### Specific points

* We agree that the inconsistency in independent filtering approaches is a problem, but they are presented in the introduction as though it was standard to filter samples one-by-one. From our understanding (and experience) most filtering methods look across samples in a dataset, which granted is still not an ideal solution. However, we believe that the filtering approach used in this preprint was to exclude rare taxa in one sample that are present in multiple other samples at higher abundance.

* Related to the above point, we thought it was odd that prevalence (i.e. the proportion of samples where an ASV is found) was not considered in the analyses, because prevalence-based filtering seems more reasonable than choosing absolute abundance cut-offs

* We also would have liked to have seen a characterization of the sparsity of de novo OTUs output by mothur compared with denoising pipelines - that are mentioned throughout the paper - as we suspect the filtering method applied in this paper would have an even more severe effect on de novo OTU abundance tables

* The importance of rarefying was stated several times in the paper but this largely was unsupported by citations and there were no comparisons with or at least acknowledgement of other normalization approaches. It was also unclear whether all of the results were based on rarefied data or not.

* Related to the above, we found the ordering of rarefying and filtering to be unclear in the methods. If the samples were rarefied prior to filtering, then the ASVs represented by a single read are not necessarily singletons (they may have had higher abundance originally). We believe many people filter rare taxa before rarefying to normalize sequencing depth and thus comparing with this approach seems appropriate.  

* We were pleased that all of the code used for analysis was available via Github, but felt that the Methods section was lacking the detail necessary to understand the analyses carried out without referring to the code repository.

* We found the assumption that singletons would increase with sequencing depth if they are artifacts to be unconvincing. Contaminants introduced by bleed-through and cross-talk would not be expected to be singletons in high depth samples for instance.

* We thought the alpha diversity results in Fig 2 were presented unclearly. We think this is a foundational result that subsequent analyses built upon, but that it is quite circular as obviously removing taxa will result in decreased alpha diversity. We do not think the fact that this result is circular was made clear in the abstract and results.

* There was also no mention or discussion at all as to the abundances that these rare taxa represented in the overall dataset - experience has shown that filtering out “rare ASVs” (that may or may not represent contaminant/spurious ASVs) can eliminate 50-90% of ASVs, yet often represents 5-10% of the overall number of reads in a sample. Conclusions reached with this remaining 90-95% of the original data are often then the same as including all ASVs. Of course, the (potentially over-inflated) richness values dive, but beta-diversity is often unaffected.

* In the alpha diversity results it would have been nice to see how a measure of evenness also changed in response to the filtering cut-offs, as Shannon is known to be more heavily weighted toward richness vs. Simpson (for example) which would be less sensitive to all the small ASV changes and would more reflect whether the overall community structure has changed significantly.

* In Fig 3 we initially were unsure how to interpret such a major shift in the coefficient of variation (COV) of the diversity metrics, but we noted that the initial COV was close to 0 in all cases. This suggests that all of the samples were extremely similar, which makes sense given that the null approach for generating the samples appears to be similar to simply distributing the reads for each ASV randomly across all samples. In addition, **this approach for generating the null samples would result in more rare taxa shared across samples than in the original data**. For example, if a taxon was originally only in one sample with a depth of 10 reads then based on the null approach (in the datasets with high sample size) it would likely be spread over 10 different samples. Accordingly, it is unsurprising that the COV would increase if rare taxa are removed (indeed there is nowhere else to go but up).

* Similarly for the results in Fig 4 we thought the comparison between the null-generated samples in one group and samples representing the original data’s composition was also unconvincing because it was comparing entirely different compositions with different distributions of rare taxa. We think it would have been more useful to compare sample groupings from each dataset to see how interpretations vary depending on filtering method. Secondly for this analysis, the random inflation of 10% of the ASVs by 5% is again going to be biased towards those rare ASVs, since they represent by far the largest number of available ASVs to randomly inflate, and therefore it is again circular that starting to remove rare ASVs from those samples will immediately crush your ability to see any differences. This is a direct by-product of basing the analyses on the null model-generated samples.

* We do not think there was sufficient description to fully evaluate Fig 5, but based on our understanding there was no normalization whatsoever of the ASV raw abundances. If this is the case, then it is totally unsurprising that you would see many false positives identified, as this is not a realistic representation of how researchers would perform these analyses in practice.

