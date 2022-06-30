# pdgfrb-thesis
Code for 2022 Semester One Honours Thesis


## Setting Up _PDGFRB_

Contains the initial code used to obtain _PDGFRB_ count data, as well as TCGA metadata.

A preliminary dataframe is established with all 11,284 TCGA samples and selected metadata including:
- Sum of counts for canonical exons 1-8 (normalised by cumulative exon length 1.714kbp)
- Sum of counts for canonical exons 9-23 (normalised by cumulative exon length 4.004kbp)
- Ratio of exon expression calculated by sum of exons 9-23/sum of exons 1-8
- Cancer type 
- TCGA ID 
- UCSC ID
- Number of total mapped counts
The dataframe is sorted by descending ratio

Also establishes counts for all TCGA samples, normalised for exon length using kbp and library size using tmc metadata for cpm at each recount3 exon

Subsets of data are created using rail_ids including
TET type ids:
 - Thymoma subtypes A, AB, B1, B2 and B3
 - Thymic carcinomas

Breakpoint (potential fusion) samplese, with samples missing exon 1 (infinite ratio) separated out

## Exon Definition Figure

Code to create 'Figure 2. Comparison of canonical and recount3 exons' from the thesis

## Exon Code 

Defines the 23 canonical exons from recount3 exons 

Created graphs of exon expression along _PDGFRB_ using exon counts for
- TET types

## Ratio Code

Defines the 22 potential canonical breakpoints within _PDGFRB_

Created graphs of exon expression along _PDGFRB_ by raio for
- All TETs
- By TET types
- Infinite/potential breakpoint samples

## Called Fusions

rail_ids for six called fusions (Table 1 in the thesis) are established
Metadata is obtained for cancer type

Created graphs of exon expression along _PDGFRB_ by:
- Exon count
- Ratios
