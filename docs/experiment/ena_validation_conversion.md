# Validation

The [FAANG validation tool](https://data.faang.org/validation/experiments) 
will validate required assay specific tabs for any of the assay types contained within the 
[FAANG experiment metadata rules](https://data.faang.org/ruleset/experiments#standard). 
You can upload your completed Experiment template in the same way as your Sample metadata template. 
This will allow the system to identify and report any errors that must be resolved before submission.
Please contact [FAANG DCC](mailto:faang-dcc@ebi.ac.uk) for 
guidance if required.

To start validation please follow these steps:

1. Click on **'Experiments''** tab
   ![Screenshot](../img/new_system/experiment/validation_service.png)

2. Click on **'Choose file''** button to choose filled out template file

3. Select the option of either making a new submission or updating existing ones.
Upon file selection, the 'Validate' or 'Reset' button is displayed. Click on the 'Validate' button to upload the file 
and run the validation service.
   ![Screenshot](../img/new_system/experiment/validation_successful.png)

4. Check **'Status'** badge for updates regarding conversion and validation. It might have three different values:
    * Waiting
    * Success
    * Errors

5. Review all **'Errors'** and **'Warnings'**. For this click on the cell
that contains any issues, pop-up window will have detailed information about
**'Errors'** and **'Warnings'**. It's also possible to download table annotated
with **'Errors'** and **'Warnings'** messages using **"Get annotated template"** 
button.
   ![Screenshot](../img/new_system/experiment/annotated_template.png)
   ![Screenshot](../img/new_system/experiment/error_and_warning.png)


**'Errors'** are problems that have to be dealt with. You will not be able to do 
a submission to the ENA if the spreadsheet contains errors. **'Warnings'** are 
items for you to review. They might be fine, but you need to decide. Any 
warnings left in a submission are likely to be reviewed by the FAANG DCC. 
You may be asked to update the experiment record later if the metadata group 
agrees a certain value should be improved.

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

You may wish to refer to [the ENA schema](https://github.com/enasequence/schema/tree/master/src/main/resources/uk/ac/ebi/ena/sra/schema) for additional information on certain 
data formats and attributes.  If there are any fields that you require and are 
missing from the excel template, please contact [FAANG DCC](mailto:faang-dcc@ebi.ac.uk) to see if we can add it.

Please contact [FAANG DCC](mailto:faang-dcc@ebi.ac.uk) if you have any issues 
in validation of your template
