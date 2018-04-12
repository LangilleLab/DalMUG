---
published: true
post_snippet: This group examined the contribution of host genetics to microbiome composition and concluded that the gut microbiome overall is not heritable, but instead is predominantly shaped by environmental factors.
title: Environment vs Genetics in Microbiome
---
 
#### [Rothschild et al., 2018, "Environment dominates over host genetics in shaping human gut microbiota." Nature](https://www.nature.com/articles/nature25973)

_Summarized from DalMUG group discussion and written by:
**Emily Lamoureux**_

### Summary

This group examined the contribution of host genetics to microbiome composition and concluded that the gut microbiome overall is not heritable, but instead is predominantly shaped by environmental factors. Using principal components to analyze samples from an Israeli cohort, Rosthchild et al. found no significant correlations between microbiome composition and self-reported ancestry and SNP profiles. They were only able to replicate 7 out of 211 previously reported associations between genetic loci and specific taxa or Bray Curtis dissimilarity using a linear mixed model. Secondly, they analyzed data from over 2000 twins using their microbiome heritability index, and only found microbiome heritability to be between 1.9% and 8.1%. Thirdly, machine learning methods were unsuccessful in predicting ancestry from microbiomes. They validated their analysis techniques on a Dutch cohort and were able to replicate similar results.
	To study microbiome-environment associations they compared the microbiomes of related and non-related individuals who had or had not shared households. While sharing a household explained a significant amount of microbiome similarity between both related and unrelated individuals, related individuals that had not shared households had no associations. 
	Lastly, the ability of the microbiome versus genetic to predict host phenotypes such as polygenic risk scores was evaluated. It was found that microbiome and genetics gave additive information in a linear model, demonstrating the independence of host genetics and microbiome composition. 

### Points of Interest

- Figure 1 pretty convincing evidence that microbiome is not shaped by host genetics
- Imputation biases?
    - Database is biased towards Europeans but since this is an Israeli cohort it should be unbiased
    - 712,542 SNPs were initially genotyped and then imputed to 5,567,647 SNPs. How much can we trust imputation? Likely pretty well. Also, individuals were stringently filtered after imputation
- Additive effects of genetics and microbiome in phenotype prediction – this agrees with our own research well
- The genotype of the LCT gene, which enables lactose consumption was the only reproducible genetic association between the microbiome composition and host genetics
- b2 value of microbiome heritability needs to be interpreted with caution since it does not account for unmeasured environmental factors that can influence microbiome composition

### Points of Confusion

- Log normalized bar chart 1C - why? Not representative of relative abundance
- Imputed SNPs – also not a lot of variation in genetic background in Israeli subjects (explains <1% of principal component plot of genetics) although methods are validated on another cohort
- Genetics can be important in a specific environment – slightly misleading
    - It could be that specific genes shape the microbiome but only in the right environmental contexts. I.e: A person has a gene that creates a deficiency in X organism but since this person does not eat foods that allow X this deficiency is not scene in the first place
- Negative results in both = congruency in methods across studies?
- Why not look at microbiome functions & host genetics associations? Have stool MGS and 16S
