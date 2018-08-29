---
title: Gut Microbiome Composition Predicts Infection Risk During Chemotherapy in Children With Acute Lymphoblastic Leukemia
post_snippet: In this report Hakim, et al., show that the composition of the gut microbiome could be used to predict if pediatric acute lymphoblastic leukemia (ALL) patients will have an infection throughout chemotherapy.
published: true
---

[Hakim et al. 2018. Gut Microbiome Composition Predicts Infection Risk During Chemotherapy in Children With Acute Lymphoblastic Leukemia. Clinical Infectious Diseases. ](https://academic.oup.com/cid/article/67/4/541/4922398)

_This is a summary of our DalMUG journal club discussion of the above paper written by [**Jacob Nearing**](https://twitter.com/JTNearing)._

### Summary
Multiple papers have now found connections between infection during treatment for hematopoietic malignancies and the composition of the patients microbiome. In this report Hakim, et al., show that the composition of the gut microbiome could be used to predict if pediatric acute lymphoblastic leukemia (ALL) patients will have an infection throughout chemotherapy. Samples were collected from 199 patients at four different timepoints throughout treatment: baseline, post induction, post consolidation, and post reinduction.
	The first question Hakim et al., wanted to answer was how the gut microbiome changed throughout treatment. They found that the diversity of the gut microbiome was significantly reduced after both induction therapy and reinduction therapy, but returned to similar levels as baseline during consolidation periods. They specifically found reductions in members of Bacteroides, Faecalibacterium spp, Ruminococcaceae, Actinobacteria, and Verrucomicrobia. They found no significant associations between antibiotic exposure time and changes within the gut microbiome suggesting that antibiotics did not play a large role in this change. 
	Next, the authors used baseline samples to help predict infection throughout chemotherapy treatment. They found no differences in diversity at baseline between patients that had infections during therapy and those that did not, but did find that patients that experienced infections had a higher abundance of Proteobacteria. They found that patients with a relative abundance of greater than 0.01% had an estimated hazard ratio of 2.12 for infection after controlling for sex, competing risk of death, and ALL relapse. Furthermore, they found that a gut microbiome composition type that was defined by the dominance of Enterococcaceae or Streptococcaceae was associated with increased risk for febrile neutropenia, diarrheal illness and any other infection outcome during treatment. 
	This is the first report on the effect of ALL chemotherapy in children to date and the first to connect the risk of infection with the composition of the gut microbiome in this population of patients. Further studies need to be done in order to determine if the gut microbiome can be used as a useful tool for infectious risk stratification in pediatric ALL patients and the mechanism behind how the composition of the gut microbiome influences infections in patients undergoing chemotherapy. 

### Points of Interest
* Interesting to see that the diversity of the gut microbiome was not different at baseline between patients that experienced infection and those that did not. This contrasts with previous results in non-Hodgkin’s Lymphoma that showed that patients with higher risks for bloodstream infections had lower gut microbial diversity [(Montassier et al., 2016)](https://genomemedicine.biomedcentral.com/articles/10.1186/s13073-016-0301-4)

* Similar to other diseases it seems that yet again Proteobacteria seem to be associated with negative outcomes

* Didn’t find changes in microbiota composition or diversity in association with antibiotic usage. Perhaps this is due to many of the highly vulnerable communities already being killed off by chemotherapeutics.

* It will be interesting to see how well their prediction model can be used in other cohorts from different geographic regions or treatment regimens.


### Points of confusion

* The group reduced their taxonomy assignment to 14 different groups at different levels of classification based on a flow chart presented in supplemental figure 2. We were confused as to how they came up with this flow chart and why it was used in the first place rather than just the taxonomy assigned by their taxonomy classifier.

* We were unfamiliar with the Youden Index, which was used to pick their Proteobacteria abundance cut off point for the prediction of infections during therapy. It seems that this method of optimization could lead to overfitting. 

* We could not figure out how they did their bootstrap validation based off of the text that was presented in the manuscript and its supplemental information. We also were unsure what features they were using during their bootstrap validation.  

