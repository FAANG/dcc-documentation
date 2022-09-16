### Prerequisite

Before submission, please validate your template using the validation service. 

### Submission endpoint

To submit your records programmatically, you can use the endpoint **https://api.faang.org/validation_submission_api/submission/TYPE/FILE_ID** with the POST HTTP method

### Path parameters

**TYPE** should be replaced with the appropriate record type, i.e. <em>samples</em>, <em>experiments</em> or <em>analyses</em>

**FILE_ID** should be replaced with the FILE_ID value used for your template during validation. This allows the API to fetch the correct template for submission.

### Request body

The request is of content-type <em>application/json</em> and the format of the request body should be as shown below.

```
{
    "username": "test",
    "password": "******",
    "mode": "test",
    "domain_name": "test-domain",
    "private_submission": false
}
```

Here, the **username** and **password** are your AAP credentials. 

The **mode** can be either <em>test</em> or <em>prod</em>. You will need to create two 
separate AAP accounts for [test](https://explore.aai.ebi.ac.uk/registerUser) and
[production](https://aai.ebi.ac.uk/registerUser) servers. 

**private_submission** can be set to <em>true</em> or <em>false</em> to indicate whether the submission is private. 

Specify the domain to be used for submission using the **domain_name** field.

A sample cURL command for submission is shown below.

```
curl --X POST 'https://api.faang.org/validation_submission_api/submission/TYPE/FILE_ID' \
-H 'Content-Type: application/json' \
--data '{
    "username": "test",
    "password": "******",
    "mode": "test",
    "domain_name": "test-domain",
    "private_submission": false
}'
--output OUTPUT_FILE_PATH
```

Here, **OUTPUT_FILE_PATH** is the path to the output file where you want to save the submission results

### Response

A response status code of 200 indicates successful submission. For samples submission to Biosamples, the response is a text file whereas for experiments and analyses submission to ENA, the response is an XML file.

A status code of 400 or 500 indicates that the submission failed, with reason for failure specified in the response body.

