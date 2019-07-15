---
published: true
title: Using reference frames enables reproducible and more accurate microbiome data analysis 
post_snippet: ...the difference in the frequency of a compositional feature can best be analyzed relative to the frequency of another individual or set of features
---

#### [Morton et al. 2019. Establishing microbial composition measurement standards with reference frames. Nature Communications.](https://www.nature.com/articles/s41467-019-10656-5)

_Summarized from DalMUG group discussion and written by: [**Gavin Douglas**](http://www.gavindouglas.ca/)_

### Summary
There is a growing awareness of the dangers of treating compositional data non-compositionally as pointed out in several recent papers
(e.g. [Gloor et al. 2017](https://www.frontiersin.org/articles/10.3389/fmicb.2017.02224/full)).
There has been a push to use tools explicitly meant for compositional data analysis (CoDa), but these more sophisticated methods
often present more of a learning curve than standard (and invalid) methods. Morton et al. add to this conversation by describing
two approaches (log-ratios and differential ranking) for conducting CoDa based on reference frames. The key idea of these approaches
is that the difference in the frequency of a compositional feature can best be analyzed relative to the frequency of another individual
or set of features. We enjoyed discussing this paper and we are convinced that shifting the field to CoDa approaches is needed.


### Points of Interest
- It’s great to hear that the multinomial regression approach can handle 0s since determining the appropriate pseudocount is an issue when using most CoDa methods.

- The tooth brushing example is great for illustrating how an increase in relative abundance != increase in absolute abundance… This could be especially useful for teaching.

- Although nothing was identified as significantly different with ALDEx2 in the tooth brushing example, it is reassuring to see that overall the coefficients agree with the multinomial model distribution.

- The atopic dermatitis example is also very convincing that reference frames provide more reliable findings overall.

### Points of Confusion
- The major question we had was how reproducibly would different researchers select reference frames and to what degree would that alter the results. The authors give some suggestions for how to choose reference frames, but we are concerned that figuring out the ideal reference frame will be impossible in most cases and would also be susceptible to p-hacking.

- It’s unclear what the consensus in the field is regarding measuring microbial load to convert relative abundances to absolute abundances. The authors make a strong argument for the need for improved CoDa methods especially for environments. where determining microbial load is difficult and for pre-existing samples. However, for most future projects determining the total microbial load per sample would avoid the problems described in this paper.

- We’re not sure why the T-statistics based on absolute and relative abundances of species agree pretty well, but the p-values are totally different.

- We’re not sure why measuring salivary flow rate was needed to estimate microbial load if flow cytometry was also performed.

- We were confused why Propionibacterium acnes was chosen as a reference frame in the atopic dermatitis example - wouldn’t it make more sense to use a prevalent species with a low log ratio?
