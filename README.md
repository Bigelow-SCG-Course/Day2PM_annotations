# Repo for Day2 PM: Annotations


![AGTC](intro_images/Picture1.png)
Comic: Zach Weinersmith
<img width="52" alt="image" src="https://user-images.githubusercontent.com/4502853/160729046-907ee6ed-1e53-4060-8e96-26362c06bf96.png">




## Genome annotation: from sequence to biology  
is the process of identifying and associating function to various segments of the assembled DNA sequence. 
It consists of three main stages:
- gene prediction
- gene identification (protein coding, ribosomal RNA genes, tranfer RNA genes) 
- identification of other genomic elements (e.g. promoters, enhancers and transcription factor binding sites)






 
 [**Prokka**](https://academic.oup.com/bioinformatics/article/30/14/2068/2390517)
 
 [**DRAM**](https://academic.oup.com/nar/article/48/16/8883/5884738)
  
  Call genes with Prodigal 
  
  ORF predicted amino acid sequences are searched against KEGG, Pfam, UniRef90 and MEROPS using MMseqs2 
  
  HHMER3 is used for HMM profile searches of dbCAN and VOGDB
  
  Include tables of the annotation outputs but Melody will explain them using the produced examples


*Maria*: Add notebook for the pipeline
  - Set the environment for prokka
  - Run prokka in ~10 SAGs (maybe each participants picks one row)
  - Set the environement for DRAM
  - Run DRAM in one SAG
  - Provide link to output for all SAGs


*Melody*: Add an extra page discussing 
  - examples of misannotations
  - how to refine annotations
