---
title: Normalization and microbial differential abundance strategies depend upon data characteristics 
post_snippet: ...this paper is an argument for the utility of rarefying data ... and a response to the “Waste Not, Want Not” paper
published: true
---

[Weiss et al. 2017. Normalization and microbial differential abundance strategies depend upon data characteristics. Microbiome.](https://microbiomejournal.biomedcentral.com/articles/10.1186/s40168-017-0237-y)

This is a summary of our DalMUG journal club discussion of this paper written by [_Gavin Douglas_](http://www.gavindouglas.ca/)

### Summary
Two (of many) important questions that arise when analyzing microbiome sequencing data are:  
* **Should the data be normalized?**  
* **How should differentially abundant (DA) features be identified?**

Weiss _et al._ explored these questions by comparing several approaches for normalizing and DA testing based on real 
and simulated 16S rRNA gene sequencing data. Unfortunately many recent tools explicitly meant for microbiome data were not 
evaluated, which highlights how quickly this field moves (the paper was published in 2017). Nonetheless, this paper does strongly 
indicate that tools originally intended for RNA-seq data, such as DESeq2, are inappropriate for microbiome data. In 
many ways this paper is also an argument for the utility of rarefying data, at least given the tools that were then available, and a 
response to the [“Waste Not, Want Not” paper](https://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1003531) by McMurdie and Holmes (2014).

### Points of Interest
* The authors did a great job of summarizing many analyses and describing the limitations of their simulations (esp. when discussing the issue of which distributions are appropriate for microbiome sequencing data).
* They clarify that rarefying data results in higher false negative rates, but not higher false positive rates as was previously described by McMurdie and Holmes. 
* The authors actually base their argument regarding rarefying data on the same simulations as McMurdie and Holmes after adjusting how the validation was performed. Apparently low-depth samples were excluded from the rarefying validation in the 2014 paper and were evaluated against all samples, which capped the possible accuracy at 85%.
* DA tools dramatically differ in terms of the numbers and intersect of which OTUs were identified as significant. This is disturbing, but agrees with similar validations we have run as well. It’s a shame that this issue still doesn’t seem to be widely understood and there still remains no clear consensus in the field for analyzing microbiome data.
* ANCOM performs especially well based on their evaluations (especially in terms of the low false-positive rate).

### Points of Confusion
* Figure 1 displays a proof-of-concept that rarefying to low depths (to 50 reads) can cause artifactual groupings if other samples are rarefied to higher depths (500 reads). Although we agree this makes sense in this extreme case we didn’t think it was realistic scenario, and it made us wonder whether there was much of an effect at higher read depths.
* Using variance-stabilizing techniques like DESeq2 for normalization results in negative numbers, which were set to 0 before calculating distances. The authors mention that this results in many rare taxa being removed, which likely accounts for the poor performance of DESeq2 normalized data. Since this normalization wasn’t intended to be used with microbiome-based metrics like UniFrac it would have been nice to see ordination based on euclidean distances. Also, would it be reasonable to add a factor to the normalized table to make all values positive? 
* A common question is whether DESeq2 can be better parameterized for microbiome data by using non-default options. It’s unclear to us how much this has been explored in general.
* Why was data rarified prior to running ANCOM - isn’t this tool explicitly intended for compositional data?
