# TRI-pore

Forensic Nanopore tri-allelic SNP sequencing

## Background

DNA analysis has become the cornerstone of contemporary forensic science. Although most forensic DNA testing still use PCR and capillary electrophoresis (CE)-based analysis methods, a transition to sequencing techniques is at hand.
Next generation targeted sequencing allows forensic scientists worldwide to harness the full potential of their DNA sample. 

## Aim

The aim of the paper (Forensic tri-allelic SNP genotyping on pooled samples using Oxford Nanopore sequencing) associating this repository was to asses the capability of Oxford Nanopore Technologies’ (ONT) handheld sequencer MinION™ to create a forensic SNP based profile. 


## Motivation

As ONT sequencing was primarerly designed to analyze long reads (>1kb) the base calling software lacks the capability to analyze short (<100bp) sequences. 
To bypass this hiatus, the short PCR amplicons were be pooled and ligated randomly to artificially create longer sequencable fragments.
This ligation protocol was furhter elaborated and a barcoding system was added, allowing for the analysis of multiple samples in one sequencing run. 
This repository contains the code to identify the barcode, split and allocate the concatenated reads into to subreads and the subsequently perform the SNP detection. 

## Methods

Illumina sequencing: Illumina sequencing was performed to generate a "true" profile
                     Data 
                     
1D & 1D2 Nanopore  :The 1D2 sequencing differs from the 1D by the fact that both the forward and reverse strand are sequencing in a 1D2                     run. This allows creation of a consensus sequence which allows to correct the sequencing errors. 
                    Variant calling on the data produced by both sequecing approaches is the identical
                    
                    A) Barcode identification
                    The barcodes are identified using a fuzzy regex allowing up to 3 sequencing errors.
                    
                    B)SNP profile generation
                    For each sample a mapping of the data against a reference databases is performed.
                    The database consists of the SNP and 25 nucleotides of the right and left flanking region
                    A table containing all variants of all loci is generated allowing SNP profile generation

## Links

Oxford Nanopore Technologies
https://nanoporetech.com/


## Contributors

Senne Cornelis,
Yannick Gansemans,
Ann-Sophie Vander Plaetsen,
Sander Willems,
Jana Weymaere,
Dieter Deforce,
Filip Van Nieuwerburgh 
