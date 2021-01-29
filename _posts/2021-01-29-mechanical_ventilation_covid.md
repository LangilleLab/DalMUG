--- 

published: true 
title: Mechanical ventilation affects respiratory microbiome of COVID-19 patients and its interactions with the host 
post_snippet: ...examine potential confounders in COVID-19 microbiome studies by analysing two datasets... the amount of time spent in the ICU and the type of oxygen support explained most of the variation in the upper respiratory tract microbiome...

--- 

[Lloréns-Rico *et al.* (2020 medRxiv preprint): Mechanical ventilation affects respiratory microbiome of COVID-19 patients and its interactions with the host.](https://www.medrxiv.org/content/10.1101/2020.12.23.20248425v1) 

_This is a summary of our DalMUG journal club discussion of this paper written by Robyn Wright_ 

### Summary

The spectrum of disease severity in COVID-19 patients is wide and the known risk factors associated with disease severity do not explain all of the variation that is observed. Early evidence suggests that the microbiome may play a role in disease progression, but there are limited studies addressing this to date. In this pre-print, Lloréns-Rico *et al.* examine potential confounders in COVID-19 microbiome studies by analysing two datasets: (1) upper respiratory tract: 16S rRNA gene (V4) amplicon sequencing data from nasopharyngeal swabs collected from 58 patients that were positive for COVID-19 and were admitted to the ICU for treatment; and (2) lower respiratory tract: scRNA-seq data from bronchoalveolar lavage samples taken from 22 COVID-19 positive patients and 13 pneumonitis controls (data taken from a previous study at the same hospital). They find that the amount of time spent in the ICU and the type of oxygen support explained most of the variation in the upper respiratory tract microbiome and that there were shifts in community structure, species- and strain-level diversity and in the relative abundance of taxa that have been previously associated with COVID-19. They also found that there were increased numbers of oral microbiota in the lower respiratory tracts of COVID-19 patients than in controls and that these may be linked with proinflammatory immune cells. This was a timely and interesting study that presents results on COVID-19 that have not (to our knowledge) previously been noted, but we had several points of confusion related to the data analysis methods used and we weren’t sure that it made sense to present the results of two relatively separate studies together in one paper.

Below are the key points that came up during our discussion. 

### Points of Interest 

- It is intriguing that the diversity was lower in samples taken from patients after discharge from the ICU, given that other studies have found that diversity recovers as the patient recovers.
- It was interesting to see the negative correlation between length of stay in ICU and diversity, but we would have liked to see it indicated which samples were taken after discharge from the ICU.
- Interesting to see only one human cell in scRNA-Seq was associated with both COVID and bacterial reads.
- It made a lot of sense to us that some of the top taxa found in the lower respiratory tract after ventilation were typical oral microbiota.

### Points of Confusion
- We were confused about the number of samples from different patients and the technical replicates included in the 16S dataset: there were 58 patients with a total of 74 swabs (not the same number of swabs as points that there were on Fig. 1a) and there were 112 samples, including technical replicates, that were sequenced (101 with >10,000 reads).
- We weren’t sure how the data were corrected for 16S copy number or decontaminated (to our understanding, there are several options within the package used) and weren’t sure what implications this had for the interpretation of data.
- It wasn’t clear whether beta diversity analyses (16S dataset) using CLR-transformations were performed on the raw or the rarefied data.
- We weren’t sure what the motivation for calculating the strain-level diversity per sample/per parameter in this way was – what effect would it have had to look at the strain-level diversity across all species rather than in 5 at random (repeated 1000 times)? Or across all samples in each parameter rather than 5 at random (repeated 100 times)? It would have been nice to have all of the data presented to see the spread of values more clearly, particularly in relation to any genera/species of interest. It also wasn’t clear in Fig. 2 that the strain-level diversity presented is not the (typically presented) number of strains in the sample – and this may be confusing for anyone that doesn’t read the methods in detail. We also would have liked to see how this differed from species/strain-level diversity calculated based on position in a phylogenetic tree rather than 97% OTU.
- We would have been interested to see the differential abundance of taxa presented at either the species or strain level, so as it correlated better with the rest of Fig. 2.
- In Fig. S2 it says that an asterisk next to the genera name indicates that the differences between ventilation type were significant after controlling for patient ID, but there were no asterisks, so we weren’t sure whether this was accidentally left off the figure or whether none of the differences were significant after correction.
- We were surprised by the low criteria for including samples (>1000) reads in the (scRNA-Seq) dataset, particularly as the 0.1% cut-off for including a species would keep a species with only 1 read in this case.
- The authors found that there was only a significant relationship between viral load and diversity when diversity was corrected for length of ICU stay, and then concluded that the conflicting results of previous studies on the relationship between viral load and diversity could be because these studies didn’t consider the effect of ventilation. We felt that this was not necessarily a fair comparison to previous studies that did report a significant relationship between viral load and diversity, as the current study only included patients that were admitted to the ICU (and therefore had relatively severe COVID symptoms) and the confliction of the previous results could also be due to sampling site (the authors mention that lower diversity was found in sputum or throat swab samples while higher diversity was found in bronchoalveolar samples).
