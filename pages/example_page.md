---
title: Genome Annotation
type: genome-annotation
contributors: [Luke Silver, Anna Syme, Mike Thang, Tiff Nelson]
description: How-to Guide for Genome Annotation with FgenesH++.
affiliation: [The University of Sydney, BioCommons Australia, Bioplatforms Australia, Galaxy Australia]
---

[Galaxy Australia](https://usegalaxy.org.au/) is capable of conducting genome annotation using the FgenesH++ annotation tool

This How-to-Guide will describe the steps required to annotate your genome on the Galaxy Australia platform (see **Fig 1**), developed in consultations between the Bioplatforms Australia [Threatened Species Initiative](https://threatenedspeciesinitiative.com/), [Galaxy Australia](https://usegalaxy.org.au/), and the [Australian BioCommons](https://www.biocommons.org.au/).

{% include callout.html type="note" content="If you need help, the Galaxy community is both approachable and helpful. [Ask them questions!](https://help.galaxyproject.org/)" %}

## Quick start guide

1. [Login to Galaxy Australia](#register-and-login)
2. Create a new history
3. Upload your assembled reference genome, repeat masked reference genome, .cdna, .pro and .dat files from transcriptome assembly workflow and the cds_from_genome.fna and pseudo_without_product.fna from a closely related species from NCBI
4. Load and execute workflows, using required options
  - FgenesH++ genome annotation: [```Fgenesh annotation-TSI```]()

5. Review workflow report and perform additional QC as needed
6. Re-run workflows, or individual tools, as needed

## How to cite the workflows

## The overall workflow
{% include image.html file="genome_annotation/overall_workflow.png" caption="Fig 1. The approach described in this How-to-Guide, including Quick Start guide steps 1) registration, 2) upload of input files, 3) FgenesH++ genome annotation Required workflow steps are blue, and optional steps are red."}

Further to this, a summary of the different elements of this assembly approach are detailed below:

| Process name     | Workflow name                             | Description                                                                          | Inputs                                                              | Outputs                                                                                                     |
| ---------------- | ----------------------------------------- | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------- |
| UPLOAD FILES     | Not applicable                            | See the [different upload options](#upload-data-files).                                     |  reference genome, repeat masked reference genome, .cdna, .pro and .dat files from transcriptome assembly workflow and the cds_from_genome.fna and pseudo_without_product.fna from a closely related species from NCBI| Uploaded data!   |
| GENOME ANNOTATION  | [Fgenesh annotation-TSI]()                         | Splitting of reference and masked reference genome files, annotation of genome using FgenesH++, merging of annotation files and extraction of mRNA, CDS and protein sequences | reference genome, repeat masked reference genome, .cdna, .pro and .dat files from transcriptome assembly workflow and the cds_from_genome.fna and pseudo_without_product.fna from a closely related species from NCBI |   GFF3 of annotated genes, fasta file of mRNA, CDS and protein sequences which were annotated  | 


## In-depth workflow guide

### Register and login

1. To register for Galaxy Australia, visit the [login page](https://usegalaxy.org.au/login).
2. Click the ```Register here``` link, as shown in **Fig 2**.
3. Complete the registration wizard and click ```Create```.
4. Login to your account!

{% include image.html file="hifi_assembly/1_register.png" caption="Fig 2. Log-in / registration menu for [Galaxy Australia](https://usegalaxy.org.au/)."%}

### Upload data file(s)
1. In Galaxy Australia, create a new history and click on ```Upload Data``` 
