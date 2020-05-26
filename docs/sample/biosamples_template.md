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
https://data.faang.org/assets/empty/faang_sample.xlsx)
* You can also download an [example template](
https://data.faang.org/assets/with_examples/faang_sample.xlsx) to refer to for advice on 
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

###### Submission tab
Provide a submission title and submission description.
* **Submission Title**. The suggested title format is 
"EBI-FAANG-HARRISON-Sheep-160414".  This is constructed from your 
organisation/group abbreviation, the "FAANG" project (to help identify your 
samples), submitters surname, common species name and date of submission.
    * **Note** please check the [organisation/group abbreviation page](../organization_group_abbreviations.md) 
    to find or add your organisation/group abbreviation for consistency across 
    institutes.
* **Submission Description**. Briefly describe the samples and study.  
This description will be displayed on BioSamples to describe all of the 
samples in your BioSamples group so it is important that it is informative 
and accurately describes the samples in the study.  **Please ensure that the 
common species name is included in this description**.

###### Person tab
Add the full details and email address of the people responsible for producing 
the data.  At least one person must be listed. For each person a role should 
be provided from the list of possible [organization roles](roles.md).

A person can have more than one role by listing them twice in full, see the 
example of John Smith below.  At least one person should be listed as the 
submitter (this is you!).

Person Last Name | Person Initials | Person First Name | Person Email | Person role
------------ | ------------- | ------------ | ------------ | ------------
Smith | J | John | john@someplace.ac.uk | submitter
Smith | J | John | john@someplace.ac.uk | experiment performer
Bloggs | LE | Laura | laura@someplace.ac.uk | data analyst

###### Organization tab
Add the full details of the organisations and funding bodies responsible for 
producing the data.  At least one organisation must be listed.

For each organisation a role should be provided from the same list as the 
person tab above.

Multiple organizations can be recorded here as appropriate, one per line.  
If an organization has more than one role, then it should be listed in full on
 multiple lines, see example for Roslin Institute below.
 
 Organization Name | Organization Address | Organization URI | Organization Role
------------ | ------------- | ------------ | ------------
EMBL-EBI | Wellcome Genome Campus, Hinxton, Cambridge, CB10 1SD, United Kingdom | http://www.ebi.ac.uk/ | curator
The Roslin Institute and Royal Dick School of Veterinary Studies | Easter Bush Campus, Edinburgh, Midlothian, EH25 9RG, United Kingdom | http://www.roslin.ed.ac.uk/ | institution
The Roslin Institute and Royal Dick School of Veterinary Studies | Easter Bush Campus, Edinburgh, Midlothian, EH25 9RG, United Kingdom | http://www.roslin.ed.ac.uk/ | biomaterial provider
BBSRC | Polaris House, North Star Avenue, Swindon, Wiltshire, SN2 1UH, United Kingdom | http://www.bbsrc.ac.uk/ | funder

###### Sample Name
Sample Name should contain a short species code, an abbreviated name for the 
institute/lab, and a unique ID for each sample, e.g. 'ECA_ROSLIN_H1'

Accepted [short species codes](short_species_codes.md) (please contact 
[FAANG DCC](mailto:faang-dcc@ebi.ac.uk) if you are submitting a species not 
listed there)

Please check the organisation/group abbreviation page to find or add your 
[organisation/group abbreviation](../organization_group_abbreviations.md) for 
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

###### Same as
BioSample ID for an equivalent sample record, created before the FAANG metadata 
specification was available. This is optional and not intended for general use, 
please contact the [data coordination centre](mailto:faang-dcc@ebi.ac.uk) 
before using it.

###### Material specific fields
For information about material specific fields please follow ruleset 
specification:

* [organism](https://data.faang.org/ruleset/samples#animal)
* [specimen from organism](https://data.faang.org/ruleset/samples#specimen)
* [pool of specimens](https://data.faang.org/ruleset/samples#pool_of_specimens)
* [cell specimen](https://data.faang.org/ruleset/samples#purified_cells)
* [cell culture](https://data.faang.org/ruleset/samples#cell_culture)
* [cell line](https://data.faang.org/ruleset/samples#cell_line)

###### Multiple values
Some metadata attributes permit multiple values. For example, you may wish to 
describe several health status traits for an animal. In this case, insert extra 
columns for the attribute into the template. Take care to copy all related 
columns. e.g. for an animal with foot and mouth disease and endocarditis, 
you would use four columns:

Health Status | Term Source ID | Health Status | Term Source ID
------------ | ------------- | ------------ | -------------
endocarditis | EFO_0000465 | foot and mouth disease | EFO_0007277

Where there isn’t a term that is precisely right, consider using the ID for a 
term that is close enough, combined with text to say exactly what you mean. 
This will be marked with a warning at validation, but you can choose to ignore 
this. You can also request a new term from the ontology. Guidance on this is 
available on the [FAANG wiki](faang_wiki.md). Contact [FAANG DCC](
mailto:faang-dcc@ebi.ac.uk) if assistance is needed. 
As requesting a new term can sometimes take a while to resolve, you can use the 
best approximation first, and update with the more accurate term at a later 
date. You don’t have to just wait for the new term to be assigned.

###### Guidelines on describing crossbred animals. 
There are [additional instructions](faang_guidelines.md) for describing 
crossbred animals 

###### Derived From / Child of 
Used to describe familial relationships between samples or what samples were 
derived from. For example, a tissue specimen is derived from an animal.

These must either:

* Refer exactly to the **'Sample Name'** of an appropriate sample within the same 
excel spreadsheet
* Refer to an appropriate sample that already exists in the **BioSamples** 
database using its BioSample ID, e.g. **'SAMEA4447799'**.

###### Specimen Collection Protocol / Purification Protocol / Cell Culture Protocol / Culture Protocol
The FAANG sample and experiment metadata specification requires your protocols 
to be publicly available.

It is best these are hosted in a location which will be available in the long 
term so locations such as lab pages are inadvisable as web addresses change 
and hosting goes away.

FAANG is happy to host protocols in the [data portal](https://data.faang.org)

If you wish FAANG to host your protocols, please send PDF copies of your 
protocols to [FAANG DCC](mailto:faang-dcc@ebi.ac.uk). Please consult the FAANG 
metadata validation privacy notice for the processing of your personal 
information in relation to protocol submission 
[https://www.ebi.ac.uk/data-protection/privacy-notice/faang-metadata-validation](
https://www.ebi.ac.uk/data-protection/privacy-notice/faang-metadata-validation)

Please name your files using this convention 
INSTITUTE_SOP_PROTOCOLNAME_YYYYMMDD.pdf e.g 
INRA_SOP_sorting_swine_CD_cells_20160504.pdf. This is a protocol for Sorting 
Swine CD cells, the protocol comes from the French National Institute for 
Agricultural Research and the protocol was written on the 4th May 2016.

Please check the [organisation/group abbreviation page](
../organization_group_abbreviations.md) to find or add your organisation/group 
abbreviation for consistency across institutes.

If you have any questions about protocols and the form they should take, 
please email the [FAANG Animal, Samples and Assays group](
mailto:faang-samples@animalgenomes.org)

## 3. Specific metadata instructions for tracking embryos and pregnancy
For samples taken from pregnant animals:

* Include that the animal was 'pregnant' in the **Sample Description**.
* The **'Animal Age At Collection'** is the age of the mother
* The gestational age and unit should also be supplied. (TODO: check this)

For embryo samples, on the **specimen from organism** sheet **'Organism Part'** 
should be listed as **"embryo"**, the **'Term Source ID'** as **"UBERON_0000922"**. 
The **'Animal Age At Collection'** should list the embryos age in days since 
conception.

## 4. Adding custom columns to your spreadsheet
It is possible to add additional custom fields to your BioSamples records, 
simply add the columns to the end of the appropriate tab.

Please contact  [FAANG DCC](mailto:faang-dcc@ebi.ac.uk) with your requirements 
as it may be something we  wish to support by default in future.

If it is possible to attach an ontology term to control the nomenclature of 
these custom fields then 'Term Source Ref' and 'Term Source ID' columns should 
also be added. If you are using an ontology not listed by default under the 
term source tab then it needs to be added to the term source tab and you also 
need to contact [FAANG DCC](mailto:faang-dcc@ebi.ac.uk) to let us know which 
ontology you have additionally used.

## 5. Missing values 
Where data cannot be included in a submission, submit one of these text values 
instead:

* not applicable
* not collected (i.e. will always be missing)
* not provided (i.e. may be added later)
* restricted access (i.e. it isn't missing, we just can't include it in a 
public document)

The use of these values will interact with the metadata validation system as 
follows:

* if an attribute is required:
    * not applicable, not collected, not provided - validation will regard 
    these as an error
    * restricted access - validation will generate a warning
* if an attribute is recommended:
    * not collected, not provided - validation will generate a warning
    * restricted access, not applicable - pass
* if an attribute is optional:
    * validation will fail with any of missing values terms. As this is an 
    optional field it should be left blank if no real data is being provided.
    
If an attribute is optional and you can’t supply it, you should just leave the 
column blank.

Assume that the DCC will ask about anything that seems implausible. e.g. 
**'restricted access'** for species would be queried.

## 6. Pools of specimens 
Each specimen within the pool should have its own specimen record.  For each 
specimen in the pool add its **'Sample Name'** (if detailed in the same file), or 
**BioSample ID** if it already exists in the BioSamples database, to the 
**'Derived From'** field.  Add as many **'Derived From'** fields as are required to 
record all of the specimens that are part of the pool.

