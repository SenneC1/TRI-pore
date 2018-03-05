# TRI-pore

Forensic Nanopore SNP sequencing

## Background

DNA analysis has become the cornerstone of contemporary forensic science. Altough most forensic DNA testing still use PCR and capillary electrophoresis (CE)-based analysis methods, a transition to sequencing techniques is at hand.
Next generation targetted sequencing allows forensic scientists worldwide to harness the full potential of their DNA sample. 

##Aim

The aim of the paper (Forensic tri-allelic SNP genotyping on pooled samples using Oxford Nanopore sequencing) associating this repository was to asses the capability of Oxford Nanopore Technologies’ (ONT) handheld sequencer MinION™ to created a forensic SNP based profile. 


## Motivation

As ONT sequencing was primarerly designed to analyze long reads (>1kb) the base calling software lacks the capability to analyze short (<100bp) sequences. 
To bypass this hiatus, the short PCR amplicons were be pooled and ligated randomly to artifically create longer sequencable fragments.
This ligation protocol was furhter elaborated and a barcoding system was added, allowing for the analysis of multiple samples in one sequencing run. 
This repository contains the code to identify the barcode, split and allocate the concatenated reads into to subreads and the subsequently perform the SNP detection. 

## Links

Oxford Nanopore Technologies
https://nanoporetech.com/


## Contributors

Senne Cornelis,
Yannick Gansemans,
Sander Willems,
Filip Van Nieuwerburgh 
