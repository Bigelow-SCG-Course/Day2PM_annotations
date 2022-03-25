# Day2PM_annotations

Maria: Add general information on annotations and databases (including caveats)
 **Prokka**
 
 **DRAM**
  https://academic.oup.com/nar/article/48/16/8883/5884738
  Call genes with Prodigal
  ORF predicted amino acid sequences are searched against KEGG, Pfam, UniRef90 and MEROPS using MMseqs2 
  HHMER3 is used for HMM profile searches of dbCAN and VOGDB


Maria: Add notebook for the pipeline
  - Set the environment for prokka
  - Run prokka in X SAGs
  - Set the environement for DRAM
  - Run DRAM in one SAG
  - Provide link to output for all SAGs

Melody: Add an extra file discussing 
  - the annotation outputs for both Prokka and DRAM
  - examples of misannotations
  - how to refine annotations
