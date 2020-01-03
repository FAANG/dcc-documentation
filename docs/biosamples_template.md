# Overview
This page will guide you through the process of submitting your samples to 
BioSamples in order to receive your sample accession IDs.  We have provided 
templates and tools to help validate your samples metadata.  If you have any 
questions about this process please contact [FAANG Data Coordination Centre](
mailto:faang-dcc@ebi.ac.uk) for 
help.

## Prerequisites
Please familiarise yourself with the [latest sample ruleset specification](
https://data.faang.org/ruleset/samples#standard) and 
the [FAANG data sharing principles](http://www.faang.org/data-share-principle).

**IMPORTANT: The data validation service is not compatible with templates 
prepared using Libre Office Calc, please use Microsoft Excel saving as xslx 
or Google sheets exporting as xslx.**

In order to submit samples to BioSamples first you need to complete Excel 
template with information about your sample following these two steps:

1. [Download the Excel template](#1-download-the-excel-template) 
2. [Complete the template](#2-complete-the-template)

## 1. Download the Excel template
* Download the latest version of the [Excel template](
https://data.faang.org/assets/faang_sample.xlsx)
* You can also download an [example template](
https://data.faang.org/assets/faang_sample.xlsx) to refer to for advice on 
completion

## 2. Complete the template
Complete the template following the instructions below on this page and 
referring to the [latest sample ruleset specification](
https://data.faang.org/ruleset/samples#standard). The rules for each 
attribute define if it is mandatory or optional, what sort of data is expected 
(numeric, date, text, etc.), what units are permitted, and whether or not an 
ontology term is required.

The Excel template contains a series of separate worksheet tabs to capture 
information about the organisms, specimens and cells. Do not alter 
or delete any of the **existing** column headings or tabs from the file.  
However it is fine to add or duplicate column headings for the purpose of 
capturing customized extra information and providing multiple values for one 
field respectively (where it's allowed, see [ruleset specification](
https://data.faang.org/ruleset/samples#standard) **"Allow multiple?"** field).

###### Sample Name
Sample Name should contain a short species code, an abbreviated name for the 
institute/lab, and a unique ID for each sample, e.g. 'ECA_ROSLIN_H1'

Accepted [short species codes](short_species_codes.md) (please contact 
[FAANG DCC](mailto:faang-dcc@ebi.ac.uk) if you are submitting a species not 
listed there)

Please check the organisation/group abbreviation page to find or add your 
[organisation/group abbreviation](organization_group_abbreviations.md) for 
consistency across institutes.

###### Sample Description
Briefly describe the sample.

###### Material and Term Source ID
For recording specimen material and term source ID please use this [table](
material_term_source_id.md)

###### Project
Always use **"FAANG"** as the project so that your samples are in the correct 
group in BioSamples.  The project tag is important, as the data coordination 
centre (DCC) will use it to find your records.

###### Availability
This is optional for all sample types. Use this to inform people how they can 
get access to the sample. This can either be as a URL, or an e-mail address to 
contact for further information. This information will persist in the archives, 
so please choose e-mail addresses or web sites that will be available for a 
long time. These are example values for the availability attribute (non-FAANG):

* https://cells.ebisc.org/EDi001-A/
* mailto:samplesgroup@example.ac.uk

###### Availability
BioSample ID for an equivalent sample record, created before the FAANG metadata 
specification was available. This is optional and not intended for general use, 
please contact the [data coordination centre](mailto:faang-dcc@ebi.ac.uk) 
before using it.