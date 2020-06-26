---
title: Subsampling large microbiome cohort highlights reproducibility issues with smaller cohorts

post_snippet:  ...typical sample sizes used in microbiome studies might simply be too low to ensure robust results. Rothschild et al. investigated this question by performing shotgun metagenomics sequencing of the stool of ~34,000 individuals...

published: true
---

[Rothschild et al. 2020. An atlas of robust microbiome associations with phenotypic traits based on large-scale cohorts from two continents. bioRxiv.](https://www.biorxiv.org/content/10.1101/2020.05.28.122325v1)

_This is a summary of our Dalhousie Microbiome User Group (DalMUG) journal club discussion of this paper written by [Gavin Douglas](http://www.gavindouglas.ca/)._

### Summary
There are often conflicting results between studies investigating links between the microbiome and human traits. One long standing potential issue has been that the typical sample sizes used in microbiome studies might simply be too low to ensure robust results. Rothschild et al. investigated this question by performing shotgun metagenomic sequencing of the stool of ~34,000 individuals from Israel and the US. The gender, age, and various blood test measures (such as cholesterol levels and a type-II diabetes biomarker) was provided by participants. The authors showed consistent significant links (across populations!) between various aspects of the microbiome and the measured human traits. They also showed that the performance of identifying reproducible associations (and of generating predictive models) based on the microbiome drops off dramatically as the sample size decreases. We enjoyed reading this preprint and believe that the implications could be extremely important.

The main points that we discussed (besides the major findings) are below.

### Points of Interest
* Great to see high consensus in the mean species relative abundance across populations
* Great to see really detailed supplementary tables and interesting idea to provide regression coefficients to allow users to come up with their own score to evaluate
* Interesting to see that the associations between the traits and alpha-diversity are relatively weak but nonetheless highly reproducible
* Extremely informative and disturbing to see that you can obtain associations that vary by two standard deviations when you subsample to 200 individuals
* Also great to see high reproducibility in correlations between traits and particular species

### Points of Confusion
* It would have been useful to see more details in the methods, like how many samples and sequencing reads were excluded at each respective step
* The abundance estimating method sounds interesting, but we did not feel we could follow it completely. For instance, the authors mention that the number of sample reads that map uniquely to each 100 read window, but isn’t that how they were defined?
* It wasn’t clear to us whether there was a gap in time between the stool collection and blood testing
* We weren’t clear what several of the blood markers, like “protein” corresponded to exactly
* We were confused why the authors show the results of the validation within the training set in Fig. 4 C-E as we felt that showing this within the test sets would have more strongly supported the major findings of their paper

### Other Points
* It would have been ideal to see how the reproducibility and performance of the approaches varied when different methods for identifying species in shotgun metagenomics data were used (like a common approach such as kraken2)
* It also would be informative to see how reproducible the identified associations are in large cohorts from different studies (to see how differences in methods contributes to issues with reproducibility)
