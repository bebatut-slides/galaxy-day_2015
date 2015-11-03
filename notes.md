Presentation notes
==================

20 mn (user session)

ASaiM: a Galaxy framework to analyze gut microbiota

Good morning, I'm Bérénice and I'm currently in post-doc.
I'm working on ASaiM: an environment to analyze gut microbiota

# Context

Before presenting ASaiM, I'll talk about the biological context: gut microbiota
    
## What is gut microbiota? Why studing it?

Gut microbiota: micro-organisms living in the gut
Seen as a forgotten organ
Important role in digestive tract
Disorder of gut microbiota related to several diseases (Chrone disease, obesity,
 cow??)
Importance to understand gut microbiota in health and also in agronomy?

## How to study it?

Advance in sequencing --> metagenomic, metatranscriptomic
    + bioinformatics treatments for taxonomic and functional assignations

On single datasets : many tools available
    QIIME, IMG/M, MG-Rast, EBI metagenomics, ...

Comparative approaches of several datasets to compare several datasets
    Examples?

But something more global: comparison of datasets from different projects

## Available data

Massive sequencing data available in public data repositories
    
Exemple: ENA, Search for "human gut metagenome"

- results: 
    - >230 studies
    - >1,540 runs
- but
    - results not easy to obtain (need to search in publications)
    - results not easy to compare: different treatements for available results
    - different metadata
    - ...

To compare different study: information from these datasets have to be collected
and formatted using a similar workflow based on specific gut microbiota db

1. Quality control
2. Sort of interesting sequences
3. Functional annotation
4. Taxonomic analysis
5. Comparative analysis

## Available tools

To format data and make them informative and standardized

several tools: QIIME, Megan, CAMERA, EBI metagenomics, CloVR-metagenomics, ...

But none follow all the requirements:

- Complete analytical workflow
- Allow gut microbiota specific datases
- Combine user-friendly interface and command-line use
- Have data management capabilities

# ASaiM

Auvergne Sequence analysis of intestinal Microbiota

An environment to analyze metagenomic and metatranscriptmic sequences from gut 
microbiota

## Components

- Database 
- Web interface to interrogate the database
- Framework

# Framework

## Objective

Bionformatics framework to generate workflow to analyze data from gut microbiota

## Constraints

- Generation of workflow with numerous tools
- Easy to use
- Flexibility
- Use of wanted/needed tools and databases

## Conception

Several tests

- Simple scripts
- Workflow managers (Airflow, ...)
- Home-made solution
- Galaxy

Choice of Galaxy

Fit with main constraints

- Generation of workflow with numerous tools
    - Workflow conception based on output/input dependencies
- Easy to use
    - Web-based interface and API 
- Flexibility
- Use of wanted/needed tools and databases
    - ToolShed 

## Galaxy instance

Tools

- From local instance
    - 
- From ToolShed
    - 
- Developed wrappers
    - Integrated in the test Tool Shed
    - 

Databases

Workflows


(in red, those to integrate)


## To do

- Add other tools, databases, workflows
- Configure FTP
- Validation
- API and BioBlend

## Documentation and GitHub

# Conclusion

# Thanks 
CPER?
Question 

