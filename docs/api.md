In the [FAANG data portal](https://data.faang.org), FAANG data is classified into three main categories: 

1. Samples including animals (the type is [organism](https://data.faang.org/organism)) and specimens (the type is [specimen](https://data.faang.org/specimen)) 
2. Experimental data including datasets (the type is [dataset](https://data.faang.org/dataset)) and files (the type is [file](https://data.faang.org/file)) 
3. Analyses (the type is [analysis](https://data.faang.org/analysis)). 

Within each type, there are two levels of data: list of records meeting certain 
criteria (filters in the left panel) and record details.

# How can I access data programmatically?
In addition to the data portal, FAANG also provides APIs which allow 
programmatic access to FAANG data.

### Endpoints
In the URI template provided below, any field which needs to be assigned with 
an actual value by the user is represented as ":field". The optional fields 
are wrapped with [ ]. There are two types of endpoints:

* List of records from one type. **https://data.faang.org/api/:type/_search/?_source=_id[&size=:size]** 
where the parameter size defines how many records are returned from the server 
and the default value is 20.
* Record detail. **https://data.faang.org/api/:type/:entityID**

### Examples
Get all available animals:
```bash
curl "https://data.faang.org/api/organism/_search/?_source=_id&size=1000"
```

Get information for animal with BioSample accession SAMEA7999918:
```bash
curl "https://data.faang.org/api/organism/SAMEA7999918"
```

Get information for sample with BioSample accession SAMEA4451650:
```bash
curl "https://data.faang.org/api/specimen/SAMEA4451650"
```

### Parse the response
The API is built on Elasticsearch, therefore the returned response is a 
typical Elasticsearch result. It is important to know where to look for 
the desired information. For the endpoint for list, the useful information can 
be found under **hits** field. The total number of return records is saved 
in the **hits.total** field while the information for each individual record 
is under **hits.hits** which is an array. If you want to retrieve all 
records from one type, you need to make sure that the value for the parameter 
**size** must be no less than the value in the **hits.total** field. 
For the endpoint for detail, the details of the record can be found under 
**_source** field

### Advanced options
The endpoints mentioned above only provide the basic functionality to make 
it possible to retrieve information for all records from one type of data. 
Elasticsearch is a powerful search platform, with many additional options 
available and described in the [Elasticsearch version 6.5 documentation](https://www.elastic.co/guide/en/elasticsearch/reference/current/search.html).

### Examples
Only return male animal records:
```bash
curl POST "http://data.faang.org/api/organism/_search/" -d '{
  "query": {
            "bool" : {
              "filter" : {
                "term" : {"sex.text" : "male"}
              }
          }
  }
}'
```

List all species stores in the data portal with counts:
```bash
curl POST "http://data.faang.org/api/organism/_search/" -d '{
    "aggs" : {
        "organism" : {
            "terms" : { "field" : "organism.text" }
        }
    }
}'
```

List all Equus caballus female species with organism part equals to liver left 
lateral lobe and FAANG standard met
```bash
curl POST "http://data.faang.org/api/specimen/_search/?_source=_id" -d '{
  "query": {
            "bool" : {
              "filter" : [
                  {"term" : {"standardMet" : "FAANG"}},
                  {"term": {"organism.sex.text": "female"}},
                  {"term": {"organism.organism.text": "Equus caballus"}},
                  {"term": {"material.text": "specimen from organism"}},
                  {"term": {"cellType.text": "liver left lateral lobe"}}
              ]
          }
  }
}'
```
From this request we found two species that meet the requirements - 
SAMEA104728881 and SAMEA104728726. Now we can list all raw data files 
associated with these records
```bash
curl "http://data.faang.org/api/file/_search/?q=specimen:SAMEA104728881&size=10000"
curl "http://data.faang.org/api/file/_search/?q=specimen:SAMEA104728726&size=10000"
```
And all analyses objects associated with these records
```bash
curl "http://data.faang.org/api/analysis/_search/?q=sampleAccessions:SAMEA104728881&size=10000"
curl "http://data.faang.org/api/analysis/_search/?q=sampleAccessions:SAMEA104728726&size=10000"
```

To use the advanced options, you need to know the data structure which is 
accessible [here](https://github.com/FAANG/faang-portal-backend/tree/master/elasticsearch). 
A useful hint for query construction, is that you can replicate the 
functionality (e.g. filtering, sorting) of the data portal search and filters. 
To do so, use your internet browsers development tools, for example in 
Google Chrome, under View menu, click Developer, then Developer tool, 
a plugin window will pop up. In the window, click "Network" tab, then 
"Headers" tab, scroll down to "Request Payload", click view source. 
The JSON can then be used in your own query by supplying after the -d in 
single quotation marks as shown above.