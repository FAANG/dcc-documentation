## Uploading Track Files

* Login to MinIO browser [http://45.88.81.38/](http://45.88.81.38/). Please contact [faang-dcc@ebi.ac.uk](mailto:faang-dcc@ebi.ac.uk) for the MinIO login credentials.

<p style="text-align: center; margin: 15px 0;">
  <img src="../../img/minio_login.png" width="65%" />
</p>

* Create a bucket with the desired track hub name.
* Upload all your track files to the bucket. The track files must be formatted in one of the compressed binary index formats supported by Genome Browsers: bigWig, bigBed, bigGenePred, bigChain, bigNarrowPeak, bigBarChart, bigInteract, bigPsl, bigMaf, hic, BAM, CRAM, HAL or VCF.

<p style="text-align: center; margin: 15px 0;">
  <img src="../../img/minio_upload.png" width="100%" />
</p>

## Filling the template

Download the [empty excel template](https://data.faang.org/assets/empty/trackhubs.xlsx). Please do not add/remove sheets or columns. You can also download the [example template](https://data.faang.org/assets/with_examples/trackhubs.xlsx) for reference and fill out the following:

<p style="text-align: center; margin: 15px 0;">
  <img src="../../img/download_trackhubs_template.png" width="75%" />
</p>

### Hub data sheet 

Fill out one row on this sheet. This information will be used to generate the hub directory and the hub.txt file for your track hub. 

1. **Name:** Name for the directory holding the track hub files. This field is mandatory.
2. **Short Label:** Short label for the track hub, with a suggested maximum length of 17 characters. This is displayed as the hub name on the Track Hubs page and the track group name on the browser tracks page. This field is mandatory.
3. **Long Label:** Descriptive label for the track hub, with a suggested maximum length of 80 characters. This is displayed in the description field on the track hubs page. This field is mandatory.
4. **Email:** Contact to whom questions regarding track hub should be directed. This field is mandatory.
5. **Description File Path:** URL to HTML page with a description of the hub's contents. This field is optional.

**Name** | **Short Label** | **Long Label** | **Email** | **Description File Path**
------------ | ------------- | ------------ | ------------ | ------------
Test Hub | test | Hub with test data | test@someplace.ac.uk | test_hub.html

### Genome data sheet 

Fill out one row on this sheet. This information will be used to generate the genomes subdirectory and genomes.txt file for your track hub.

1. **Assembly Accession:** Genome assembly accession with GCA prefix. This field is mandatory.
2. **Organism:** Name of the organism which is displayed along with the description on title page in the genome browser. This field is optional.
3. **Description:** Descriptive text to be displayed on the gateway page and title page in genome browser. This field is optional.

**Assembly Accession** | **Organism** | **Description** 
------------ | ------------- | ------------ 
GCA_000003025.6 | Pig | Pig genome 

### Tracks data sheet 

Fill out one row for each track file that you have uploaded to MinIO storage. This information will be used to generate the trackDb.txt file for the hub, to organise your track files into subdirectories, and to associate the track files to the related FAANG specimen records.

1. **Track Name:** Symbolic name of the track, which must be unique for each track file. The first character must be a letter, and the remaining characters must be letters, numbers, or under-bar ("_"). This field is mandatory.
2. **File Path:** Path to the track file on MinIO storage. It should be of the format <BUCKET_NAME>/<FILE_NAME>. This field is mandatory.
3. **File Type:** Format of the track file. It must be either bigWig, bigBed, bigBarChart, bigGenePred, bigInteract, bigNarrowPeak, bigChain, bigPsl, bigMaf, hic, bam, halSnake or vcfTabix (Note: use type bam for CRAM files).  This field is mandatory.
4. **Short Label:** Short name for the track with a suggested maximum length of 17 characters. It is displayed in the configuration and track settings, and on the details pages in the Genome browser. This field is mandatory.
5. **Long Label:** Descriptive label for the track with a suggested maximum length of 80 characters. It is displayed in the configuration and track settings, and on the details pages in the Genome browser. This field is mandatory.
6. **Related Specimen ID:** BioSample ID of a FAANG Specimen to which this track is associated. This will allow the trackhub to be linked to the specimen record in the FAANG Data Portal. This field is mandatory.
7. **Subdirectory:** Name of the subdirectory in which this track will be organised in the hub. All tracks can also be in the same subdirectory. This field is mandatory.

**Track Name** | **File Path** | **File Type** | **Short Label** | **Long Label** | **Related Specimen ID** | **Subdirectory**
------------ | ------------- | ------------ | ------------ | ------------ | ------------ | ------------
Track1 | test-hub/test1.Bigbed | bigBed | t1 | test track 1 | SAMEA104728908, SAMEA104728909 | sub_dir1
Track2_1 | test-hub/test2_1.Bigbed | bigBed | t2.1 | test track 2.1 | SAMEA104728909, SAMEA104728910 | sub_dir2
Track2_2 | test-hub/test2_2.Bigbed | bigBed | t2.2 | test track 2.2 | SAMEA104728907 | sub_dir2

## Submitting Track Hub

### Upload Template 

Upload the filled out template using the file uploader on the Track Hubs submission page. 

<p style="text-align: center; margin: 15px 0;">
  <img src="../../img/upload_trackhub.png" width="75%" />
</p>

### Validation 

* The template is converted and validated. You can see the status of the submission beside the file uploader. 

<p style="text-align: center; margin: 15px 0;">
  <img src="../../img/trackhub_validation.png" width="100%" />
</p>

* Any validation errors are reported in the “Validation Results” section. Error messages at the top of the section indicate which sheets have errors. Navigate between different tabs, corresponding to each sheet in the excel file, to view the table with cells having errors highlighted in red. Click on a cell to get a description of the error. 

<p style="text-align: center; margin: 15px 0;">
  <img src="../../img/trackhub_errors.png" width="85%" />
</p>

* Once the template has passed initial validation, hub files are generated and the “HubCheck Results” subsection displays any errors/ warnings reported by the UCSC hubCheck program.

<p style="text-align: center; margin: 15px 0;">
  <img src="../../img/hubcheck_results.png" width="100%" />
</p>

* All errors need to be fixed, but warnings maybe ignored after reviewing.

### Submission

* After all errors are fixed, the submission button is enabled. Click on the submit button to register your track hub with the Track Hub Registry. 
* If registration is successful, your track hub will be searchable in the genome browsers. The track hub is then also associated with related FAANG specimen records based on the information provided in the template.

<p style="text-align: center; margin: 15px 0;">
  <img src="../../img/trackhub_submission.png" width="100%" />
</p>
