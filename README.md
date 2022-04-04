# Repo for Day2 PM: (Functional) Annotations



<img src="https://github.com/Bigelow-SCG-Course/Day2PM_annotations/blob/main/intro_images/Picture1.png" width="650"> 
Comic: Zach Weinersmith





## Genome annotation: from sequence to biology  
Annotation is the process of identifying and associating function to various segments of the assembled DNA sequence. 
It consists of three main stages:
- gene prediction
- gene identification (protein coding, ribosomal RNA genes, tranfer RNA genes) 
- identification of other genomic elements (e.g. promoters, enhancers and transcription factor binding sites)


In this tutorial, we will use two different annotation pipelines, [**Prokka** (Seeman, 2014)](https://academic.oup.com/bioinformatics/article/30/14/2068/2390517) and  [**DRAM** (Shaffer et al. 2020)](https://academic.oup.com/nar/article/48/16/8883/5884738)



## Prokka
[Prokka](https://github.com/tseemann/prokka) is the first command line software tool to fully annotate bacterial, archeal and viral genomes. Prokka relies on external feature prediction tools to identify the coordinates of genomic features within contigs. 


<img src="https://github.com/Bigelow-SCG-Course/Day2PM_annotations/blob/main/intro_images/Prokka_table1.png" width="500">

For the protein coding genes, the function is infered by comparison to databases of known proteins in a hierarchical matter. Briefly, prokka first searches, using [BLAST+](https://bmcbioinformatics.biomedcentral.com/articles/10.1186/1471-2105-10-421), three (small but well curated) databases, [ISfinder](https://www-is.biotoul.fr/index.php), [NCBI Bacterial Antimicrobial Resistance Reference Gene Database](https://www.ncbi.nlm.nih.gov/bioproject/313047), [UniProtKB (SwissProt)](https://www.uniprot.org/uniprot/). Then [HMMER3](http://hmmer.org) is used for similarity searching against protein family profiles (mostly bacterial specific).

### Output files
<img src="https://github.com/Bigelow-SCG-Course/Day2PM_annotations/blob/main/intro_images/Prokka_ouput.png" width="500">
  
  
## DRAM
[DRAM](https://github.com/WrightonLabCSU/DRAM) has been recently developed for the annotation of genomes and viral contiges. Besides the identification of individual genes, DRAM attemps to put information into context i.e. to assign them to metabolic pathways. Predicted amino acid sequences are searched against [KEGG](https://www.kegg.jp), [Pfam](https://pfam.xfam.org), [UniRef90](https://www.uniprot.org/uniref/) and [MEROPS](https://www.ebi.ac.uk/merops/) using [MMseqs2](https://github.com/soedinglab/MMseqs2). Additionally, HHMER3 is used for HMM profile searches of [dbCAN](https://bcb.unl.edu/dbCAN2/) and [VOGDB](https://vogdb.org).

<img src="https://github.com/Bigelow-SCG-Course/Day2PM_annotations/blob/main/intro_images/DRAM_outline.png" width="650">
  


## Let's get started
- First let's clone this repository into your own working directory. To do so, open up a terminal window and type the following commands:
```
$ cd ~/storage/user_lab/{your_username_here}/
$ git clone https://github.com/Bigelow-SCG-Course/Day2PM_annotation.git
```
- [Annotations.ipynb](https://github.com/Bigelow-SCG-Course/Day2PM_annotations/blob/main/Annotations.ipynb): Then, we will run both Prokka and DRAM in a subset of SAGs.
- [DRAM_results_mrl.ipyn](https://github.com/Bigelow-SCG-Course/Day2PM_annotations/blob/main/DRAM_results_mrl.ipynb): Briefly explore DRAM output files.
- [SCGC_course_day2PM_outputsandmisannotations_03312022.pdf](https://github.com/Bigelow-SCG-Course/Day2PM_annotations/blob/main/SCGC_course_day2PM_outputsandmisannotations_03312022.pdf): Dive deeper into the DRAM result and annotation caveats.

## Other Methods for Annotating Genomes
Other than Prokka and DRAM, there are some other programs used to annotate genomes (in similar ways)
- [EggNOG mapper](https://hpc.nih.gov/apps/eggNOGmapper.html#:~:text=eggNOG%2Dmapper%20is%20a%20tool,ideally%20suited%20for%20functional%20inference.)
- [METABOLIC](https://github.com/AnantharamanLab/METABOLIC)
- [MicrobeAnnotator](https://github.com/cruizperez/MicrobeAnnotator)
- [BlastKOALA/GhostKOALA/KofamKoala](https://www.kegg.jp/blastkoala/)
