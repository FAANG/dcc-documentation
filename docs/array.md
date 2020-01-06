# Submission of array data
Please refer to the submission guidelines from [ArrayExpress](
https://www.ebi.ac.uk/arrayexpress/submit/overview.html) and [GEO](http://www.ncbi.nlm.nih.gov/geo/info/submission.html) for the 
details of how to submit to these archives. The FAANG-specific aspects of submission are:

1. Regardless of which archive you use, please ensure that you create 
    BioSamples records (see [guidance](biosamples_template.md)) ahead of 
    submitting data, and use the BioSample accessions in your submissions. 
    The details of how to refer to BioSamples are set out below. BioSamples 
    accessions will start with SAMEA...
2. Follow the [FAANG experiment metadata guidelines](
https://data.faang.org/ruleset/experiments#standard) for experiments.

### BioSamples in ArrayExpress
The ArrayExpress submission system does not directly cater for the use of 
existing BioSamples accessions. Notify the ArrayExpress curators and explain 
that you wish to reuse existing BioSamples entries in your submission. They 
will provide further guidance.

### GEO
Please add a new column in the SAMPLES section titled "BioSample ID" and 
include the SAM ID number for each sample. This will alert the curator 
handling your submission to link your records to each appropriate BioSample.

When you submit your data to GEO, please include in the notification email the 
fact that you have already generated BioSample IDs and have included them in 
the metadata spreadsheet.