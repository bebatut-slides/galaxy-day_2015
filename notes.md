Presentation notes
==================

20 mn (user session)

ASaiM: a Galaxy framework to analyze gut microbiota

Good morning, I'm Bérénice and I'm currently in post-doc in Clermont-Ferrand.
I'm working on ASaiM: an environment to analyze gut microbiota

# Context

Before presenting ASaiM, I'll talk about the biological context of the project: the gut microbiota
    
## Gut microbiota

### What is it? 

Gut microbiota: numerous micro-organisms living in the gut

### Why studing it?

Seen as a forgotten organ
Important role in digestive tract
Disorder of gut microbiota related to several diseases (Chrone disease, obesity)
Importance to understand gut microbiota in health and also in agronomy?

## Study

### Meta-omic

Advance in sequencing --> metagenomic, metatranscriptomic of a sample of these 
micro-organisms

Sequencing of genetic material without any organism culture, without information
about organisms

Bioinformatics treatments for taxonomic and functional assignations and then 
determine which organisms are present in a gut sample, what are they doing and how

### Comparative meta-omics of different samples

To understand how microbiota is working, need to compare several samples with 
comparative approaches 

Li et al 2014: Comparison of the relative abundance of several taxons in 2 populations
(chinese and danish) --> difference in gut microbiota given the country, the diet...

### Comparative meta-omics of different samples from different projects

For a global view, need to compare different samples from different projects...

Massive sequencing data are available but not exploited in public data repository 
such as ENA, NCBI, ...
    
Exemple: ENA, Search for "human gut metagenome"

- results: 
    - >230 studies
    - >1,540 runs
- but
    - results not easy to obtain (need to search in publications)
    - results not easy to compare: different treatements for available results
    - different metadata
    - ...

To compare different studies/projects: information from these datasets have to be collected
and formatted using a similar workflow based on specific gut microbiota db

1. Quality control
2. Sort of interesting sequences
3. Functional annotation
4. Taxonomic analysis
5. Comparative analysis

Several tools: QIIME, Megan, CAMERA, EBI metagenomics, CloVR-metagenomics, ...

But none of them follows all the requirements:

- Complete analytical workflow
- Allow gut microbiota specific datases
- Combine user-friendly interface and command-line use
- Have data management capabilities

# ASaiM

We are developping ASaiM: An environment to analyze metagenomic and metatranscriptomic 
sequences from gut microbiota

## Components

- Database to take a census of gut microbiota data 
- Web interface to interrogate the database
- Framework

# Framework

The gut microbiota data are analyzed using several steps. Each of these steps
corresponds to a tool.

For example, gut metatranscriptomic data must follow a workflow corresponding to
the one in the example

Need to interface the tools together to automize the analyses

ASaiM framework: Bionformatics framework to generate workflow for analyses of 
gut microbiota data

## Constraints

- Generation of workflow for analyses using numerous tools, each for a dedicated task
- Easy use (by biologist and on numerous datasets)
- Flexibility and modularity (in tool and parameters)
- Incorporation of wanted/needed tools and databases (specific to gut data)

## Conception

Several tests

- Simple Python scripts to interface several tools
- Workflow managers (Airflow, ...) to generate workflow based on task dependencies
- Home-made solution
    - a configuration to describe the workflow
    - configuration file generated using a web interface
    - python scripts to execute workflow
    - home-made solution is not a good solution (to develop, to maintain, ...)
- Galaxy instance

Choice of Galaxy

Fit with main constraints

- Generation of workflow with numerous tools
    - Galaxy wrappers : as many tools as we want to develop wrappers 
    - Workflow conception based on output/input dependencies
- Easy to use
    - Web-based interface and API 
- Flexibility and modularity
- Incorporation of wanted/needed tools and databases
    - ToolShed
    - wrappers : as many tools as we want to develop wrappers 

## Galaxy instance

Instance based on standard Galaxy but with only "usefull" tools sorted given their
use for microbiota data

Instance available on Github

To launch:
    - clone
    - install the required tools such as pip
    - lauch the instance using a dedicated script
    - visualize it

Behind the launch_galaxy.sh script: shell script to configure the instance

## Choices

In the instance, the tools are coming from

- From standard Galaxy instance
- From ToolShed
- Developed wrappers
    - Misc to manipulate sequence files for example
    - Integrated in the test Tool Shed
    - In development

Workflows: currently in construction given the tool integration

Databases (automatically integrated)

- SortMeRNA
- COG
- To add

To help in tools, database, workflow, ... we write a documentation available
with readthedocs
I'm trying to write the doc during development

## To do

Use of Galaxy helps the development of this instance.

But, there is several things to do

- Add other tools, databases, workflows
- Validate workflows
- Configure FTP
- API and BioBlend

# Conclusion

# Thanks 
CPER?
Question 

