---
published: true
title: Ratio of primary to secondary bile acids is a clear biomarker of pediatric Crohn’s disease activity

post_snippet: ...patients who remained in remission following EEN for up to 24 weeks were dominated by secondary bile acids, whereas other patients were mainly dominated by primary bile acids
---

[Connors et al. 2019. The relationship between fecal bile acids and microbiome community structure in pediatric Crohn’s disease. The ISME Journal.](https://www.nature.com/articles/s41396-019-0560-3)

_This is a summary of our DalMUG journal club discussion of this paper written by [Gavin Douglas](http://www.gavindouglas.ca/)_

### Summary
This paper (published by our frequent collaborators at Dalhousie University) focused on identifying biomarkers of sustained remission
in a cohort of pediatric Crohn’s disease (CD) cohort. These patients were all undergoing exclusive enteral nutrition (EEN) treatment,
which has previously been shown to be a successful treatment for CD. The major finding was that patients who remained in remission
following EEN for up to 24 weeks were dominated by secondary bile acids, whereas other patients were mainly dominated by primary bile
acids. This study was based on only 17 patients (with multiple time-points for each), but nonetheless convincingly shows that bile
acids are an important biomarker of CD. This study also sets the stage for investigating whether bile acids are a mechanistic link
between CD and the microbiome.

### Points of Interest
- Interesting to see a range of clinical metrics distinguishing the patients over treatment (e.g. erythrocyte sedimentation rate and platelet counts in addition to the weighted pediatric Crohn’s disease activity index).
- Clear qualitative difference in proportion of secondary vs primary bile acids based on patient remission state
- Assemblages identified by BioMico are a nice way of visualizing the taxonomic differences between primary and secondary bile acid samples… We need to try this out!
- Useful to summarize Spearman correlations between taxa and bile acids by counts per phylum - makes interpretation much easier and makes the difference between 16S and metagenomics easy to spot
- Identifying taxa encoding genes involved with metabolizing primary bile acids seems promising and it will be interesting to see this explored in larger cohorts

### Points of Confusion
- The posterior probabilities shown in the network figure seem low, but we’re not sure what a reasonable cut-off would be when identifying BioMico assemblages
- Also we were confused about how it would work for a taxon to have a high posterior probability of being a member of multiple assemblages (e.g. Bacteroides_4)
- We were unclear whether metagenomics-identified taxa were based on the standard MetaPhlan2 pipeline or not (once again interesting to see the low taxa count either way)
- We were unclear why significant taxa were identified with Kruskal-Wallis tests after running BioMico - was this mainly a sanity check that BioMico was performing well?
- No or almost no negative associations between bile acids and taxa were identified - we found this a little surprising, but could biologically make sense
- It wasn't clear to us how the taxonomic contributors of _bsh_ and other bile acid processing genes were identified
