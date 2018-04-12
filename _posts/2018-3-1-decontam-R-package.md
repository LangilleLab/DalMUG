---
published: true
post_snippet: ...designed to classify features into contaminant or non-contaminant categories based on one or two deterministic patterns observed in empirical data
title: decontam - an R package to remove microbial sequencing contaminants
---

#### [Davis et al., 2018. Simple statistical identification and removal of contaminant sequences in marker-gene and metagenomics data. BioRxiv.](https://www.biorxiv.org/content/early/2017/11/17/221499)

_Summary of DalMUG group discussion written by:
**Molly Hayes**_

### Summary
Metagenomic and 16S data are contaminated with sequences that do not correspond to members of the microbial community under study. In this preprint, Davis, Proctor, Holmes, Relman and Callahan (2017) present their R package decontam, which is designed to classify features into ‘contaminant’ or ‘non-contaminant’ categories based on one or two deterministic patterns observed in empirical data. The first pattern takes advantage of the idea  that the frequency with which contaminant sequences are observed tends to be inversely proportional to the total DNA concentration in a sample, whereas the frequency of ‘true’ sequences is independent of DNA concentration. Taking any type of feature abundance data as well as a DNA quantitation data as inputs, decontam fits two simple linear regression models to each feature—a ‘contaminant’ model with slope -1, and a ‘non-contaminant’ model with slope 0—and uses an F-test (in which the null hypothesis is that the true slope is 0) to perform model selection. 

The second pattern exploited by decontam is the tendency for contaminant sequences to be more prevalent in negative controls than in actual samples; taking feature abundance data from samples and negative controls as inputs, a Fisher’s exact test (or its chi-squared approximation) is performed on each 2x2 contingency table expressing presence vs. absence of a given feature across negative controls vs. samples (in which the null hypothesis is that the row groups and column groups are independent). 

The p-values from these frequency- or prevalence-based tests are then compared to a user-determined cutoff value in order to classify features as those arising from contaminant vs. non-contaminant sequences. The authors applied decontam to several datasets, including 16S data from the oral mucosa, 16S and MGS data from a dilution series of a Salmonella bongori monoculture, 16S data from placental biopsy samples, and 16S data from a study of the relationship between the vaginal microbiome and pre-term births. 


### Points of Interest
* decontam was found to perform well at classification in the first two datasets (as compared with previous observations from oral 16S data or expected content of the monoculture dilutions, respectively).
* Batch effects across different extraction kits and sequencing centers in the dilution series data were reduced after removal of contaminant features.
* decontam provided some support for the theory that the observed placental microbiome may be an artefact of contamination, although the presence of Ruminococcaceae remains unexplained.
* Several taxa found in previous work to have significant associations with pre-term birth were called as contaminants rather than true members of the vaginal microbiome, which suggests that decontam could be used to relieve some of the statistical burden of multiple comparisons.
* The authors note that the method cannot account for cross-contamination, that the assumptions of the frequency-based test are not satisfied in low-biomass samples, and that the method has low sensitivity when a contaminant is present in only a few samples.


### Points of Confusion
* Contamination can happen at multiple stages of microbiome profiling (e.g. sample collection, DNA extraction, DNA amplification/library prep, sequencing) and detecting these will require DNA concentrations or controls for different stages. The manuscript is not clear on what type of contamination is being detected or when the controls and DNA concentrations are being collected.
* Just as the authors recommend that samples from different environments be decontaminated separately, they might address whether this also applies to cases and controls, since there is evidence that bacterial biomass differs systematically between healthy participants and those with certain diseases (e.g., IBD).
* The procedures used by the package to compute composite p-values from frequency- and prevalence-based tests were not outlined in the Methods.
* Were pseudo-counts imputed for zero entries before taking logarithms?
* The number of negative controls should be similar to the number of true samples in order for the prevalence-based test to have sufficient power; prospective users should be guided more explicitly on this point.
* Should it be specified that the positions of negative controls on the plate be randomized so as to satisfy independence assumptions? 
* At several points the authors discuss p-value thresholds for classification that are much higher than any appropriate significance level, and the distributions of p-values from each type of test on each dataset are not provided; users may need more guidance on avoiding false-positive contaminant identification.

