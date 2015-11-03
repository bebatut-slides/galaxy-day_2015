Galaxy Day 2015
===============

# Title

ASaiM: a Galaxy framework to analyze gut microbiota data

# Abstract

Massive sequencing data from intestinal microbiota are avaiable in public data 
repositories (Genbank, ENA, …) but are not easy to identify with associated 
metadata, query and compare because they are dispatched and possibly 
underwent different analyses. 

To extract useful information from these datasets, they need to be collected and 
formatted using a similar workflow based on specific gut microbiota databases.

To process and analyze data from gut microbiota, we developed a framework based 
on a personalized Galaxy instance. In this instance, several tools are 
incorporated (PRINSEQ, FastQ-Join, SortMeRNA, Reago, usearch, framebot, cd-hit, 
MetaPhlAn, HUMAnN, QIIME), with databases such as COG (Clusters of Orthologous 
Groups of proteins) or the catalog of reference genes in the human gut 
microbiome (Li et al, Nature Biotechnology, 2014). We defined some standard 
workflows using these tools and databases.
