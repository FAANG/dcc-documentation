# Submit the XML files to ENA
1. Register for an ENA submission account if you do not already have one 
[https://www.ebi.ac.uk/ena/submit/sra/#registration](https://www.ebi.ac.uk/ena/submit/sra/#registration)
    * More detailed instructions on account registration can be found here 
    [http://ena-docs.readthedocs.io/en/latest/reg_01.html](
    http://ena-docs.readthedocs.io/en/latest/reg_01.html)
2. Upload your sequencing data to your account area
    * Follow one of the submission methods detailed on the following page 
    [http://ena-docs.readthedocs.io/en/latest/upload_01.html](
    http://ena-docs.readthedocs.io/en/latest/upload_01.html)
        * The main options are to use the webin Java client, FTP transfer or 
        the Aspera client. These will require you to have registered for an 
        ENA submission account first.
        * Please read this page and make sure to use one of the supported 
        file formats [http://ena-docs.readthedocs.io/en/latest/format_01.html](
        http://ena-docs.readthedocs.io/en/latest/format_01.html)
    * Remember you will need to provide md5 checksum value for every file you 
    upload to ensure the integrity of uploaded file, 
    see [http://ena-docs.readthedocs.io/en/latest/upload_01.html#file-md5-checksums](http://ena-docs.readthedocs.io/en/latest/upload_01.html#file-md5-checksums)
    * If you have a large number of files to upload, you may want to create a 
    manifest file that can then be supplied to aspera 
    (using '--file-list=/PATH/TO/FILELIST’) for example to list which files 
    need to be uploaded.  This can be created programatically in unix using a 
    command similar to 'find /PATH/TO/BASESEQUENCINGDIRECTORY -name "*.fq" > 
    asperafilelist.txt’.
3. Verify XML validity using the ENA test service 
([https://www-test.ebi.ac.uk/ena/submit/drop-box/submit/](https://www-test.ebi.ac.uk/ena/submit/drop-box/submit/)). 
More detailed submission programatic instructions are here 
[http://ena-docs.readthedocs.io/en/latest/prog_01.html#](http://ena-docs.readthedocs.io/en/latest/prog_01.html#) 
    * Choose your experiment.xml, run.xml, study.xml and submission.xml files 
    from the zip folder created by the conversion tool.
    * Input your username and password, username will be something like "Webin-45144".
    * Fix any errors that the test service reports, please contact 
    [faang-dcc@ebi.ac.uk](mailto:faang-dcc@ebi.ac.uk) if you have any issues 
    that you cannot resolve.
    * Keep resubmitting until no more errors reported, should see **/RECEIPT/@success="true"**.
4. Once you have passed the test service continue to submission with ENA 
production service ([https://www.ebi.ac.uk/ena/submit/drop-box/submit/](https://www.ebi.ac.uk/ena/submit/drop-box/submit/))
    * Choose your experiment.xml, run.xml, study.xml and submission.xml files from the zip folder created by the conversion tool.
    * Input your username and password, username will be something like "Webin-45144".
    * Fix any errors that the test service reports, please contact 
    [faang-dcc@ebi.ac.uk](faang-dcc@ebi.ac.uk) if you have any issues that you 
    cannot resolve.
    * Keep resubmitting until no more errors reported, should see **/RECEIPT/@success="true"**.
5. Receive and store XML receipt
    * Once a submission has been processed a receipt XML is returned that 
    conforms to the [SRA.receipt.xsd](ftp://ftp.sra.ebi.ac.uk/meta/xsd/latest/SRA.receipt.xsd) schema. 
    If the submission was successful then the returned XML contains **/RECEIPT/@success="true"**.
    * If there were any errors then the XML contains **/RECEIPT/@success="false"**.
    * For more information please see [http://ena-docs.readthedocs.io/en/latest/prog_01.html#receipt-xml](http://ena-docs.readthedocs.io/en/latest/prog_01.html#receipt-xml)
6. Check for validation fails post submission (files are not checked until 
after submission), so it may be some time before you are emailed regarding 
any errors or success.

Please contact [FAANG DCC](mailto:faang-dcc@ebi.ac.uk) if you have any issues with any of the processes on this page.