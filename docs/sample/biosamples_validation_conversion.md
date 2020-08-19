# Validation

The filled out template can be validated against the FAANG rules, using the 
[on-line tool](https://data.faang.org/validation/samples). It will provide a 
report highlighting problems for review. This is under development, so please 
query [FAANG DCC](mailto:faang-dcc@ebi.ac.uk) if you have any concerns about 
the validation result.

To start validation please follow these steps:

1. Click on **'Choose file''** button to choose filled out template file
2. Click on **'Upload a File'** button to upload template to validation service
![Screenshot](../img/validation_service_workflow.png)

3. Check **'Status'** badge for updates. It might have three different values:
    * Waiting
    * Success
    * Errors
4. If status has **'Success'** value you can start validation. For this click
on **'Start validation'** button
5. Check **'Status'** badge in **'3. Validation results:'** section for updates.
It might have three different values:
    * Waiting
    * Success
    * Errors
6. Review all **'Errors'** and **'Warnings'**. For this click on the cell
that contains any issues, pop-up window will have detailed information about
**'Errors'** and **'Warnings'**. It's also possible to download table annotated
with **'Errors'** and **'Warnings'** messages using **"Get annotated template"** 
button.
![Screenshot](../img/annotated_template.png)

![Screenshot](../img/error_and_warning.png)


**'Errors'** are problems that have to be dealt with. You will not be able to 
start a submission to the BioSamples if the spreadsheet contains errors. 
**'Warnings'** are items for you to review. They might be fine, but you need 
to decide. Any warnings left in a submission are likely to be reviewed by the 
FAANG DCC. You may be asked to update the sample record later if the metadata 
group agrees a certain value should be improved.

For descriptions and explanations of the different error messages that the 
validation tool can provide please see [FAANG validation error message 
explanations](../faang_validation_error_message_explanation.md).

Having run the validation tool on your spreadsheet, you will need to update it 
to deal with the errors shown. Review the warnings and consider making changes 
to deal with these. Re-validate your spreadsheet, and repeat the process until 
there are no errors left and you are comfortable with everything that has 
triggered a warning. If there are some things that you cannot resolve, 
contact [FAANG DCC](mailto:faang-dcc@ebi.ac.uk) for help. Eventually, you will 
have a set of metadata that passes the validation checks and is ready for 
submission.
