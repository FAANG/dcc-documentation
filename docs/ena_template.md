# Overview
This page will guide you through the process of submitting your sequencing 
data to [European Nucleotide Archive (ENA)](https://www.ebi.ac.uk/ena) using 
RESTful method. How to use Webin-CLI to make the submission will be updated 
very soon. In this document, ENA and the read archives are used interchangeably 
and other reads databases will be referred individually by their names. 
If you have any questions about this process please contact 
[FAANG Data Coordination Centre (DCC)](mailto:faang-dcc@ebi.ac.uk) for help. 

## Prerequisites
1. You must have already [submitted your sample information](
biosamples_template.md) and obtained your 
BioSample accessions ahead of submitting sequencing data.  You must then use 
these FAANG BioSample accessions in your sequencing data submissions to the 
read archives. Your BioSample accessions start with SAMEA followed by a 
unique number.
2. Determine which archive is most appropriate for your assay data, if in 
doubt please contact [FAANG DCC](mailto:faang-dcc@ebi.ac.uk) for guidance.
3. Read the [FAANG experiment metadata guidelines](
https://data.faang.org/ruleset/experiments#standard) and gather the required 
information to meet the standards, this may require you to contact your 
sequencing centre for example. The template below can be useful for gathering 
this information prior to starting the submission process. The template can 
also be used with the [FAANG conversion tool](
https://data.faang.org/validation/experiments) to create the XML documents 
required for submission to the [European Nucleotide Archive (ENA)](
http://www.ebi.ac.uk/ena).

**IMPORTANT: FAANG is not supported by the [ENA webin based submission process](https://www.ebi.ac.uk/ena/submit/sra/#home). 
FAANG experiment data must be submitted to ENA using the process described on 
this page that involves submission to [ENA dropbox submission](https://www.ebi.ac.uk/ena/submit/drop-box/submit/)**

**You must be able to find your records by searching the BioSamples accession 
in the search box at the top right corner of BioSamples web pages before 
submitting any experimental assays, which indicates that your samples have 
been properly indexed and searchable by ENA. This process normally takes 
about 24 hours, but may take longer in peak periods.**

Steps required to submit sequencing data:

1. [Download the Excel template](#1-download-the-excel-template) 
2. [Complete the template](#2-complete-the-template)

## 1. Download the Excel template
* Download the latest version of the [Excel template](
https://data.faang.org/assets/faang_experiment.xlsx)
* You can also download an [example template](
https://data.faang.org/assets/faang_experiment.xlsx) to refer to for advice on 
completion

Please refer to [ENA guidance](http://www.ebi.ac.uk/ena/submit) on the requirements for submission and to the 
latest [experiment ruleset specification](https://data.faang.org/ruleset/experiments#standard). The rules for each attribute define 
if it is mandatory or optional and what sort of data is expected (numeric, 
date, text, etc.).

The above template can be used to gather the required information to meet the 
FAANG experimental standards.  It is also possible to use this template with 
the [FAANG conversion tool](https://data.faang.org/validation/experiments) to 
generate the required XML documents for submission to 
[European Nucleotide Archive (ENA)](http://www.ebi.ac.uk/ena). You will 
currently have to manage your own submission to other archives and for more 
complex data types, but please contact [FAANG DCC](mailto:faang-dcc@ebi.ac.uk) 
to see if we can help you with your submission or look into supporting your 
requirements in future releases.

**IMPORTANT: The data validation service is not compatible with templates 
prepared using Libre Office Calc, please use Microsoft Excel saving as xslx or 
Google sheets exporting as xslx.**

This spreadsheet is divided into a number of tabs within which the required 
information is gathered to record Submission, Study, Experiment and Run 
information for an ENA submission.  It also can be useful for gathering 
information for submission to other archives by just completing the 
relevant assay specific tab e.g. 'RNA-seq'.  
Do not alter or delete any of the column headings or tabs from the file.

Guidance for completion of this template for submission to the 
[European Nucleotide Archive (ENA)](http://www.ebi.ac.uk/ena) is further down 
this page.  If you have any questions about the use of this template please 
contact [FAANG DCC](mailto:faang-dcc@ebi.ac.uk) for help.

## 2. Complete the template