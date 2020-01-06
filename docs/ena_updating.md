# Update existing submission in ENA
1. Read the ENA instructions for the latest advice here 
[http://ena-docs.readthedocs.io/en/latest/programmatic.html](http://ena-docs.readthedocs.io/en/latest/programmatic.html) 
look for the sections on update.
2. Ensure that you have used the same SUBMISSION alias as your previous 
submission.  Change your submission XML file so that the actions block is 
the following (removing the add and release statements):

```
<ACTIONS>
    <ACTION>
         <MODIFY/>
     </ACTION>
 </ACTIONS>
```

3. Verify XML validity using the ENA test service 
([https://www-test.ebi.ac.uk/ena/submit/drop-box/submit/](https://www-test.ebi.ac.uk/ena/submit/drop-box/submit/))
    * Choose your experiment.xml, run.xml, study.xml and submission.xml files 
    from the zip folder created by the conversion tool.
    * Input your username and password, username will be something like "Webin-45144".
    * Fix any errors that the test service reports, please contact 
    [faang-dcc@ebi.ac.uk](mailto:faang-dcc@ebi.ac.uk) if you have any issues 
    that you cannot resolve.
    * Keep resubmitting until no more errors reported, should see **/RECEIPT/@success="true"**.
4. Once you have passed the test service continue to submission with ENA 
production service ([https://www.ebi.ac.uk/ena/submit/drop-box/submit/](https://www.ebi.ac.uk/ena/submit/drop-box/submit/))
    * Choose your experiment.xml, run.xml, study.xml and submission.xml files 
    from the zip folder created by the conversion tool.
    * Input your username and password, username will be something like 
    "Webin-45144".
    * Fix any errors that the test service reports, please contact 
    [faang-dcc@ebi.ac.uk](mailto:faang-dcc@ebi.ac.uk) if you have any issues 
    that you cannot resolve.
    * Keep resubmitting until no more errors reported, should see **/RECEIPT/@success="true".**
5. Receive and store XML receipt
    * Once a submission has been processed a receipt XML is returned that 
    conforms to the [SRA.receipt.xsd](ftp://ftp.sra.ebi.ac.uk/meta/xsd/latest/SRA.receipt.xsd) schema.
    If the submission was successful then the returned XML contains **/RECEIPT/@success="true"**.
    * If there were any errors then the XML contains **/RECEIPT/@success="false"**.
    * For more information please see 
    [http://ena-docs.readthedocs.io/en/latest/prog_01.html#receipt-xml](http://ena-docs.readthedocs.io/en/latest/prog_01.html#receipt-xml)
    
Check for validation fails post submission (files are not checked until 
after submission), so it may be some time before you are emailed regarding any 
errors or success.

Please contact [faang-dcc@ebi.ac.uk](mailto:faang-dcc@ebi.ac.uk) if you have 
any issues with any of the processes on this page.