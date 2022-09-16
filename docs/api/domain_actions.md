The Domain actions API can be used to submit new domains or view a list of existing domains in the AAP server for Biosamples submission.

## Create new domain

To create a new domain for Biosamples submission, use the endpoint **https://api.faang.org/validation_submission_api/domain_actions/submit_domain** with HTTP POST method.

The request is of content-type application/json and the format of the request body should look like this -

```
{
    "username": "test_user",
    "password": "******",
    "mode": "test",
    "private_submission": false,
    "domain_name": "test-domain",
    "domain_description": "test domain"
}
```

Here, the **username** and **password** are your AAP credentials. 

The **mode** can be either <em>test</em> or <em>prod</em>. You will need to create two 
separate AAP accounts for [test](https://explore.aai.ebi.ac.uk/registerUser) and
[production](https://aai.ebi.ac.uk/registerUser) servers. Credentials from one 
account won't work on another.

**private_submission** can be set to <em>true</em> or <em>false</em> to indicate whether the domain is used for a private submission. Specify the name and description for your new domain in the **domain_name** and **domain_description** fields, respectively.

The cURL command for the above request would look like this -

```
curl -X POST 'https://api.faang.org/validation_submission_api/domain_actions/submit_domain' \
-H 'Content-Type: application/json' \
--data '{
    "username": "test",
    "password": "*****",
    "mode": "test",
    "private_submission": false,
    "domain_name": "test-domain",
    "domain_description": "test domain"
}'
```

If a new domain is successfully created, you will get a response with status code 200. A status code of 400 or 500 indicates that the domain creation failed, with reason for failure specified in the response.

## List existing domains

To view a list of existing domains, use the endpoint **https://api.faang.org/validation_submission_api/domain_actions/list_domains** with HTTP POST method.

The request is of content-type application/json. The request body format is as shown below, and the fields are same as specified for the <em>submit_domain</em> endpoint. 

```
{
    "username": "test_user",
    "password": "******",
    "mode": "test",
    "private_submission": false,
}
```

The cURL command for the above request would look like this -

```
curl -X POST 'https://api.faang.org/validation_submission_api/domain_actions/list_domains' \
-H 'Content-Type: application/json' \
--data '{
    "username": "test",
    "password": "*****",
    "mode": "test",
    "private_submission": false
}'
```






