--- 

published: true 
title: Critical Assessment of Metagenome Interpretation - the second round of challenges
post_snippet: ...to test a range of different tools commonly used for metagenomic assembly, genome binning, taxonomic binning and taxonomic profiling...this work is really useful for the microbiome community, but we felt that there were several aspects of the writeup that could be improved upon...

--- 

[Meyer *et al.* (2021 BioRxiv preprint): Critical Assessment of Metagenome Interpretation – the second round of challenges](https://www.biorxiv.org/content/10.1101/2021.07.12.451567v1) 

_This is a summary of our DalMUG journal club discussion of this paper written by Robyn Wright_ 

### Summary

This study used newly generated simulated samples to test a range of different tools commonly used for metagenomic assembly, genome binning, taxonomic binning and taxonomic profiling. Meyer *et al.* have extended the results from the first CAMI challenge by sequencing genomes from a plant root environment, a marine environment and clinical or murine gut strains. Meyer *et al.* used these newly sequenced genomes to simulate both long and short read metagenome samples from the marine or plant root environments and for a “strain madness” dataset (where they include multiple strains of the same species). They then asked the authors of bioinformatic tools to download the challenge datasets (simulated metagenomic samples) and to provide the results obtained by their tool as well as all parameters and settings used to run the tool. Altogether, over 5000 submissions from 76 programs were included here. The study then discusses the results for each challenge – assembly, genome binning, taxonomic binning and taxonomic profiling – using a range of different metrics to determine the “best” performing program in each category. We were pleased to see an update to the previous CAMI study, and this work is really useful for the microbiome community, but we felt that there were several aspects of the writeup that could be improved upon in order to increase the clarity and presentation of this study.

Below are the key points that came up during our discussion. 

### Points of Discussion

* There were some parts of the manuscript where it would be useful for the method to be detailed more fully, even though it is the same method used in their previous study (for example, when the results mention the creation of the gold standard assemblies)
* There were several abbreviations used that we thought detracted from the readability (e.g., mismatches, MEGAHIT assemblies, gold standard assemblies)
* Much of the results were quite difficult to read because they jumped quickly between the metrics and tools being discussed
* The figures were quite difficult to interpret:
    - Figure 1: would be much easier to read if the radar plots were replaced with line or bar graphs – for example, in panel a, some of the values for SPAdes and A-STAR look quite similar, but as they are not next to each other it is impossible to compare
    - Figure 2: providing a summary for each tool across the different datasets would have been very useful, there is a lot of information here and it is quite overwhelming
    - Figure 3: not a comment on the graph itself but we were confused about how the average completeness is in many cases lower at the domain level than the phylum level
* While most metrics used were explained in the methods section (apart from the NGA50, which we had not previously come across), we didn’t really understand why some were given different names than what is typically used in the field. For example, while using the terms completeness and purity made sense when assessing assembly or genome binning performance, recall and precision are what these are typically termed in methods assessing taxonomic binning or profiling performance. Likewise, we didn’t know why the L1 norm and weighted unifrac distance metrics were termed “error”. This caused us to search for what made this error metric different from the distance that we are used to seeing, before realising that these were just given a different name. Given that most readers will not read a paper from start to finish, sticking to standard terminology used by the field would make reading much easier.
* While we were really pleased to see simulated metagenome samples that were closer to environmental samples, we thought that because the samples used genomes from isolates that there will be a bias towards taxa that can be easily cultured and that are therefore more likely to be in databases already. We don’t really see a good alternative to this (although including genomes with a simulated greater Average Nucleotide Identity to the databases could help), but we did think that this should maybe be pointed out.
* While we do understand that choosing the best tool can be a little subjective as the metrics that matter most may depend on the question that you are asking of your data, we would have liked the authors to have made more of an attempt to do this, particularly for the taxonomic binning/profiling. Some solid recommendations in the conclusions section would be nice.
* We can appreciate that the parameters used to run each tool are just what was submitted by the challenge participants, however, we would have liked to see more on how this impacted the results. For example, Kraken2 (which we are very familiar with) has a confidence threshold that can be set and – in our experience – increasing this slightly probably would have drastically increased the precision (purity) while not changing the recall (completeness) very much. Knowing that this may be true for one tool just made us question how the results might change if the parameters used were optimised more for each program. Likewise, the database used for all tools was just the NCBI RefSeq nt database, and we wondered what impact including the full RefSeq database would have had on the results.
* We weren’t sure that it was very useful to look at the taxonomic profilers/binners as an average across ranks – if they didn’t perform at the higher taxonomic ranks then this would obviously be really problematic, but it is the lower ranks that would generally be the focus anyway.
* In the methods for the taxonomic profiling, it was mentioned that each program was given a rank, but we didn’t see mention/graphing of these ranks in the results.
