--- 

published: true 
title: The use of taxon-specific reference databases compromises metagenomic classification 
post_snippet: ...by replacing the fungal database of HMS with 18 species of amphibians and reptiles (i.e. organisms not expected to be present in the human gut microbiome) and applying this to the human gut metagenome samples used in the previous paper, they are able to identify these species...

--- 

[Marcelino *et al.* 2020. The use of taxon-specific reference databases compromises metagenomic classification. BMC Genomics](https://bmcgenomics.biomedcentral.com/articles/10.1186/s12864-020-6592-2) 

This paper is published as Correspondence to: 
[Soverini *et al.* 2019. HumanMycobiomeScan: a new bioinformatics tool for the characterization of the fungal fraction in metagenomic samples. BMC Genomics](https://bmcgenomics.biomedcentral.com/articles/10.1186/s12864-019-5883-y) 

_This is a summary of our DalMUG journal club discussion of this paper written by Robyn Wright_ 

### Summary of HumanMycobiomeScan: a new bioinformatics tool for the characterization of the fungal fraction in metagenomic samples 

This paper introduces a new pipeline for the classification of fungi within metagenome samples (primarily those taken from the human gut). The authors constructed a database using all complete fungal genomes available in the NCBI database in February 2018, which included 1213 entries that corresponded to 66 different fungal genomes. Their pipeline consists of three key steps: 
1. Mapping of reads to fungal reference genomes using Bowtie2 
2. Filtering out bacterial, human and low-quality reads using BMTagger 
3. Mapping of remaining reads to fungal reference genomes using Bowtie2 

The authors report that when they apply HumanMycobiomeScan (HMS) to mock communities they are able to correctly identify the 20 fungal species within this community and that HMS is more accurate in profiling this mock community than either BLASTn or MG-RAST. The authors then apply HMS to profile the mycobiome of stool metagenome samples from 11 Italians and 27 Hazda hunter-gatherers from Tanzania. Here they report that they find fungi in 37 of these 38 samples and that they detect 65 of the 66 species in their fungal reference database within these samples. 

### Summary of The use of taxon-specific reference databases compromises metagenomic classification 

In this correspondence the authors argue that “using reference databases comprised of a single taxonomic group leads to an unacceptably high number of false-positives due to: (i) mapping to conserved genetic regions in reference genomes, and (ii) sequence contamination in the assembled reference genomes”. They demonstrate that by replacing the fungal database of HMS with 18 species of amphibians and reptiles (*i.e.* organisms not expected to be present in the human gut microbiome) and applying this to the human gut metagenome samples used in the previous paper, they are able to identify these species in at least 12 samples each. The authors then use their own tool, CCMetagen to taxonomically classify these samples using the entire NCBI nucleotide database. They report that, among the eukaryotes identified, there are obvious misclassifications of some reads as insects, mollusks and plants. After filtering these out, they report fungi in only three of these samples, while 21 have other microbial eukaryotes. Of the fungi, the most abundant class is the Saccharomycetes, with 36 reads, while the other two classes had two reads and one read assigned to them. They investigate some of the fungal classifications made by HMS and find that of the 101 sequences found in one sample, 85% were rRNA genes, 11% unspecified genomic regions and 4% were protein coding genes. We felt that the authors of this correspondence were fairly critical of HMS specifically – when there are a reasonable number of other similar pipelines available – but that this was an important study to demonstrate the need for reference databases that encompass more than just the taxa of interest.   

Below are the key points that came up during our discussion. 

### Points of Interest 

- We thought it was really interesting to see that you can more-or-less identify any species that you look for, if the database that you use for searching is narrow enough 
- It was also interesting to see that many of the potential misclassifications reported here may originate from problems with parts of the genomes within reference databases  

### Other Points 
- It would have been nice to see how some of the more commonly used tools for metagenome taxonomic assignment had performed (e.g. Kraken2), in both papers 
- It would be interesting to see how implementing a reference database that includes a wider range of taxa but is still reduced (e.g. to a single genome per genus or family) would perform 
