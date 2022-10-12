### Prerequisite

Before using the validation service, you will need to fill out an excel template with details of your records. For more information about filling the template, please refer to the **Completing the template** page in the respective sections of the documentation depending on the record type.

### Validation endpoint

To validate your filled out template against the FAANG ruleset programmatically, you can use the endpoint **https://api.faang.org/validation_submission_api/validation/TYPE** with the POST HTTP method

### Path parameter

**TYPE** should be replaced with the appropriate record type, i.e. <em>samples</em>, <em>experiments</em> or <em>analyses</em>.

For example, use **https://api.faang.org/validation_submission_api/validation/samples** for validating samples.

### Query parameter

To get an annotated excel file with the validation results, use the query parameter **annotate_template** with value <em>true</em>. If value is <em>false</em>, or if the query parameter is not specified, you will get a JSON response containing the validation results.

For example, **https://api.faang.org/validation_submission_api/validation/samples?annotate_template=true** returns an excel file with validation errors and warning annotated on your template. 

**https://api.faang.org/validation_submission_api/validation/samples?annotate_template=false** or **https://api.faang.org/validation_submission_api/validation/samples** will return the validation results in JSON format.

### Request

The Content-type is <em>multipart/form-data</em>.
The body has a file_id as the key and the location to your template file as the value.

For example, the cURL command for validating samples and saving the annotated template is as follows.

```
curl -X POST 'https://api.faang.org/validation_submission_api/validation/samples?annotate_template=true'
--form 'FILE_ID=@"PATH_TO_TEMPLATE_FILE"'
--output OUTPUT_FILE_PATH
```

**FILE_ID** is a unique ID for your template file. You will need this ID for the submission step.

**PATH_TO_TEMPLATE_FILE** is the path to your template file on your local system.

**OUTPUT_FILE_PATH** is the path to the output file where you want to save the validation results

### Response

The validation results may contain errors and warnings.  Before proceeding to submission step, errors need to be fixed, but addressing the warnings is not mandatory for submission. 

If you choose an annotated file type response, you can see the errors and warnings highlighted on the excel file as shown below.

<p style="text-align: center; margin: 15px 0;">
  <img src="../../img/val_err_annot.png" width="45%" />
  <img src="../../img/val_warn_annot.png" width="45%" />
</p>

The errors and warnings in JSON format response are displayed as shown below.

<p style="text-align: center; margin: 15px 0;">
  <img src="../../img/val_err_json.png" width="75%" />
</p>

<p style="text-align: center; margin: 25px 0;">
  <img src="../../img/val_warn_json.png" width="75%" />
</p>

For more information on the errors and warnings, refer to the documentation for **Validation** in the respective sections depending on the record type.

