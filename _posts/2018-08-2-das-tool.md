---
title:  Das Tool - Aggregate method of metagenome assembly outperforms individual methods
post_snippet: ...a new method of aggregating the results of multiple metagenome assembly programs together to produce a better set of assemblies.
published: true
---

[Sieber et al. 2018. Recovery of genomes from metagenomes via a dereplication, aggregation and scoring strategy. Nature Microbiology. ](https://www.nature.com/articles/s41564-018-0171-1)

_This is a summary of our DalMUG journal club discussion of the above paper written by [**Gavin Douglas**](https://twitter.com/gavin_m_douglas)._

### Summary
Das Tool is a new method of aggregating the results of multiple metagenome assembly programs together to produce a better set of assemblies. This tool uses a consensus approach that tends to output more and higher-quality bins than if individual assembly programs were used alone. If you’re too busy to read the paper you can check out [this video](https://www.youtube.com/watch?v=CIQETV30_u8&feature=youtu.be&t=210) that illustrates how Das Tool increases the number of bin.

Overall we were convinced that using this tool would be better than using a single metagenome assembly program. One possible drawback is that since Das Tool is agnostic to where the input bin sets came from it may prove difficult to compare the output assemblies reported in different publications! Also, since this tool measures genome completeness based on known universal single-copy genes it can’t be used with viral assemblies.

### Points of Interest
* Great summary of the problem of metagenome assembly from their intro: “The challenge of recovering genomes from complex mixtures of sequence fragments is comparable to that of assembling jigsaw puzzles from a mixture of many puzzles without knowing how many puzzles are present and what they look like.”
* CAMI challenge data was used for validation, which several of us weren’t familiar with - these datasets seem great for validating shotgun metagenome analysis tools 
* Interesting to see comparison with “Binning_refiner” which is a similar tool published recently - based on their analyses this tool has much lower performance
* Also interesting to hear of BUSCO, which is a less conservative method to measure completeness than CHECKM
* Nice to see a comparison of the different assembly tools along with Das Tool and interesting that there is no clear trend in which performs best (except maybe for MaxBin2)

### Points of Confusion
* It wasn’t clear to us how the cut-offs were chosen that were used to discard the individual bins that did not overlap across different bin sets
* Reporting precision and recall along with F1 scores would have been nice for comparing tool performance
* Interesting to see how many genomes were assembled in each environment (e.g. Das Tool found 340/596 high-quality genomes in high complexity environment. MaxBin2 was second best with 276/596); however, this was difficult to evaluate without more details on the read depths and abundances of the genomes in each environment
* The authors showed that no metagenome assembly program performed best across all datasets, but nonetheless it would have been nice to have clear suggestions on which programs should be used with Das Tool if only for consistency in the future
* Related to the above - it would have been interesting to see how performance would have changed if a single metagenome assembly program was re-run multiple times with different parameter settings. For instance, running MaxBin2 with 10 different --prob_threshold options and then inputting these bin sets to Das Tool.
* We weren’t sure what the penalty for megabins referred to in the score calculation
