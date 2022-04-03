# Repo for Day2 PM: (Functional) Annotations



<img src="https://github.com/Bigelow-SCG-Course/Day2PM_annotations/blob/main/intro_images/Picture1.png" width="550"> 
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

For the protein coding genes, the function is infered by comparison to databases of known proteins in a hierarchical matter:
  
  
  
  DRAM
  ORF predicted amino acid sequences are searched against KEGG, Pfam, UniRef90 and MEROPS using MMseqs2 
  
  HHMER3 is used for HMM profile searches of dbCAN and VOGDB
  
  Include tables of the annotation outputs but Melody will explain them using the produced examples


## Let's get started
- First let's clone this repository into your own working directory. To do so, open up a terminal window and type the following commands:
```
$ cd ~/storage/user_lab/{your_username_here}/
$ git clone https://github.com/Bigelow-SCG-Course/Day2PM_annotation.git
```
- [Annotations.ipynb](https://github.com/Bigelow-SCG-Course/Day2PM_annotations/blob/main/Annotations.ipynb): Then, we will run both Prokka and DRAM in a subset of SAGs.
- [DRAM_results_mrl.ipyn](https://github.com/Bigelow-SCG-Course/Day2PM_annotations/blob/main/DRAM_results_mrl.ipynb): Breifly explore DRAM output files.
- [SCGC_course_day2PM_outputsandmisannotations_03312022.pdf](https://github.com/Bigelow-SCG-Course/Day2PM_annotations/blob/main/SCGC_course_day2PM_outputsandmisannotations_03312022.pdf): Dive deeper into the DRAM result and annotaion caveats.
