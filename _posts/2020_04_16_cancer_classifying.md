---
published: true
title: Classifying cancer with microbial sequences in the TCGA and metagenomics data

post_snippet: ...screened for microbial DNA and RNA in thousands of samples from The Cancer Genome Atlas… and demonstrated that the microbial sequences could be used to distinguish between cancer types
---

[Poore et al. 2020. Microbiome analyses of blood and tissues suggest cancer diagnostic approach. Nature.](https://www.nature.com/articles/s41586-020-2095-1)

_This is a summary of our DalMUG journal club discussion of this paper written by [Gavin Douglas](http://www.gavindouglas.ca/)_

### Summary
Poore et al. screened for microbial DNA and RNA in thousands of samples from The Cancer Genome Atlas (TCGA). Microbial DNA/RNA made up 2.5% of reads on average, which normally from a human perspective would be considered contaminants. They applied machine learning methods and demonstrated that the microbial sequences could be used to distinguish between cancer types. They also demonstrated that the microbial sequences could be used to distinguish between more specific sample groupings, such as between early and late stage cancers and tumour vs normal tissue. Overall we thought this paper was a good proof-of-concept that this approach could be a useful complement to existing sequence-based cancer classification methods. However, further validation is needed and additional clarification of several points would have been nice to avoid readers misinterpreting the implications.

Below are the key points of interest and confusion that came up during our discussion.


### Points of Interest
- Nice to see application of SHOGUN and bwa to verify kraken taxonomic results
- Great browser for exploring the data. However, there was some concern that this would allow misleading associations to be mined by cancer biologists, who might not be familiar with the data limitations, when generating hypotheses.
- Great to see precision-recall curve results as well as ROC (although sample size of each comparison would have been nice to visualize)
- Interesting that not more H. pylori identified in stomach cancer tumours compared to normal tissue
- Convincing result that the microbial sequences can effectively distinguish samples where DNA sequencing of tumour cannot (such as with early stage samples only)
- We were especially convinced by the blood-based modeling because several of us thought this data would be less contaminated and potentially more useful clinically as non-invasive early detection testing

### Points of Confusion
- Given that the TCGA RNA-seq datasets underwent poly-A tail selection would this not greatly affect how the microbial component of this data is interpreted? It would have been nice to see this discussed.
- We believe kraken1 was used instead of the latest version - we were unsure why this tool was chosen instead of a tool like Pathoscope or PathSeq
- Unclear how many features were used to train the machine learning models. Some of us thought that the very high AUC performance values could indicate that the models were being overfitted.  
- Unclear what negative blanks correspond to in the TCGA
- Why not use other cancer microbiome datasets (particularly colon cancer microbiome datasets) as validation of their approach?
