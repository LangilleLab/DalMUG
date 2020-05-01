---
published: true
title: Clustering co-abundant genes identifies components of the gut microbiome that are reproducibly associated with colorectal cancer and inflammatory bowel disease

post_snippet: ...addressed the problem of high dimensionality in metagenomics data by clustering genes using the Approximate Nearest Neighbour algorithm to form co-abundant gene groups, or CAGs
---

[Minot and Willis 2019. Clustering co-abundant genes identifies components of the gut microbiome that are reproducibly associated with colorectal cancer and inflammatory bowel disease. Microbiome.](https://microbiomejournal.biomedcentral.com/articles/10.1186/s40168-019-0722-6)

_This is a summary of our DalMUG journal club discussion of this paper written by Robyn Wright_


### Summary
Minot & Willis addressed the problem of high dimensionality in metagenomics data by clustering genes using the Approximate Nearest Neighbour algorithm to form co-abundant gene groups, or CAGs. They use different colorectal cancer (CRC) and inflammatory bowel disease (IBD) datasets as “discovery” and “validation” cohorts with the aim of identifying CAGs that are associated with either disease or health in these cohorts. They identify thousands of CAGs that contain between 2 and 23,856 genes and show that of those identified in the discovery cohorts as associated with either disease or health, 44% and 97.2% were validated for the CRC and IBD datasets, respectively (i.e. also associated with disease/health in the validation cohort). The CAGs that were validated in the IBD dataset were dominated (98.5%) by CAGs that were more abundant in healthy participants while the CRC dataset was much more balanced between CAGs that were more abundant in healthy or diseased participants. They were able to identify several CAGs that correspond to taxa or KEGG orthologs known to have links with the diseases and suggest that this approach may be used to identify strains that contain the genes that are identified within these CAGs. Overall, we felt that this paper presented an interesting approach that could be tested out in the future, but we thought that it could have benefited from further validation against other commonly used approaches for detecting differentially abundant taxa or functions and that it was let down by the figures not being well explained. 

Below are the key points of interest and confusion that came up during our discussion.


### Points of Interest
- An interesting approach to reducing the dimensions of metagenomic data and therefore reducing the computational challenges in analysing such data.
- It was interesting to see the steps used for analysis numbered in this way as we hadn’t previously seen methods written like this. It was also nice to see such a focus on ensuring that the methods used here would be reproducible. 
- They show fairly convincingly that the CAGs identified as associated with health/disease are reproducible across multiple datasets.
- Good to see the biological relevance of the identified CAGs although this would be strengthened by knowing how the discussed CAGs were chosen.

### Points of Confusion
- Fig. 2: What do the different colours in A-D mean? Is positive/negative estimated coefficient associated with disease or health? (We guessed positive is healthy, based on the large numbers of healthy IBD CAGs mentioned in text). What are the circular lines in A-D? Why are the colours different for disease/health in the CRC and IBD datasets in E-F? What are the estimated coefficients for the CAGs shown in E-F? Why were these CAGs shown?
- Fig. 3: We weren’t sure how the taxonomic assignments for CAGs in A-B were determined – were they a consensus? As in Fig. 2, is positive/negative estimated coefficient associated with disease or health? How were the KOs shown in A-B chosen? For C-D we would have liked to also see what proportion of the genome the genes that were more or less abundant in CRC/IBD represented. We also couldn’t work out how the genes were shown – were these all genes identified here? How were they ordered? Is the ordering the same as the dendrogram in Fig. 1?
- The paper presents a method for identifying biologically relevant units that may be associated with disease or health, but we weren’t sure why they didn’t validate this against other approaches. For example, we weren’t sure why random genes from CAGs were shown for Fig. 2 C-D and thought that either taking a gene from the middle of a CAG or comparing all genes would have been more convincing that this method is an improvement on others that are commonly used.
- It would have been interesting to know whether the CAGs that were identified as healthy were the same in both CRC and IBD datasets.
- They rely heavily on the assumption that CAGs are likely to mainly contain genes from similar organisms, but we didn’t really feel that they had proven this.
