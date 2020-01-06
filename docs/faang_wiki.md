# Guidance for use and creation of ontology terms

### How to search for an existing ontology term
Many attributes require a term from a specified ontology. The purpose of this 
is to ensure that the project uses a consistent vocabulary to describe the 
samples.

The Ontology Lookup Service ([http://www.ebi.ac.uk/ols/index](
http://www.ebi.ac.uk/ols/index)) allows you to perform text searches that will 
guide you to selecting appropriate ontology terms. To find a term:

1. Type your search query into the text box and hit search.
2. You can filter down to particular ontologies using the 'Filter by ontology' 
menu on the left of the screen. 
3. Clicking upon the most relevant term will take you to the specific page for 
that term.
4. You can use the tree view, to navigate to more and less specific terms to 
find the most appropriate term for what you are describing.

FAANG utilises a number of different ontologies.  For initial guidance on the 
selection of appropriate ontologies for each section of the submission forms 
please consult [latest ruleset specification](
https://data.faang.org/ruleset/samples#standard)

###### List of ontologies used in FAANG

* OBI [http://purl.obolibrary.org/obo/](http://purl.obolibrary.org/obo/)

    **An integrated ontology for the description of life-science and clinical 
    investigations**.  This ontology will support the consistent annotation of 
    biomedical investigations, regardless of the particular field of study. 
    The ontology will represent the design of an investigation, the protocols 
    and instrumentation used, the material used, the data generated and the type 
    analysis performed on it.
    
* NCBI Taxonomy [http://www.ncbi.nlm.nih.gov/taxonomy](http://www.ncbi.nlm.nih.gov/taxonomy)

    **An ontology representation of the NCBI organismal taxonomy**.  The 
    Taxonomy Database is a curated classification and nomenclature for all 
    of the organisms in the public sequence databases. This currently 
    represents about 10% of the described species of life on the planet.
    
* EFO [http://www.ebi.ac.uk/efo/](http://www.ebi.ac.uk/efo/)

    **A systematic description of many experimental variables available in 
    EBI databases **. It combines parts of several biological ontologies, 
    such as UBERON anatomy, ChEBI chemical compounds, and Cell Ontology. 
    The scope of EFO is to support the annotation, analysis and visualisation 
    of data handled at the EBI.
    
* LBO [http://bioportal.bioontology.org/ontologies/LBO](
http://bioportal.bioontology.org/ontologies/LBO)

    **A vocabulary for cattle, chicken, horse, pig and sheep breeds**.
    
* PATO [http://purl.obolibrary.org/obo/pato](http://purl.obolibrary.org/obo/pato)
    **An ontology of phenotypic qualities (properties, attributes or 
    characteristics)**.  This ontology can be used in conjunction with other 
    ontologies such as GO or anatomical ontologies to refer to phenotypes. 
    Examples of qualities are red, ectopic, high temperature, fused, small, 
    edematous and arrested.
    
* VT [http://bioportal.bioontology.org/ontologies/VT](http://bioportal.bioontology.org/ontologies/VT)

    **An ontology of traits covering vertebrates**.  Measurable or observable 
    characteristics pertaining to the morphology, physiology, or development 
    of vertebrate organisms.
    
* ATOL [http://www.ebi.ac.uk/ols/beta/ontologies/atol](http://www.ebi.ac.uk/ols/beta/ontologies/atol)
    **An ontology of characteristics defining phenotypes of livestock in their 
    environment**. Provide a reference ontology of phenotypic traits of farm 
    animals for the international scientific and educational - communities, 
    farmers, etc.; - deliver this reference ontology in a language which can 
    be used by computers in order to support database management, semantic 
    analysis and modelling; - represent traits as generic as possible for 
    livestock vertebrates; - make the ATOL ontology as operational as possible 
    and closely related to measurement techniques; - structure the ontology in 
    relation to animal production.
    
* EOL [http://www.ebi.ac.uk/ols/beta/ontologies/eol](http://www.ebi.ac.uk/ols/beta/ontologies/eol)
    **Environment and rearing system ontology for livestock animal dedicated to production, including fish**.
    
* UBERON [http://uberon.github.io/](http://uberon.github.io/)
    **An integrated cross-species anatomy ontology covering animals and 
    bridging multiple species-specific ontologies**.  Uberon is an anatomical 
    ontology that represents body parts, organs and tissues in a variety of 
    animal species, with a focus on vertebrates.
    
* CL [http://www.ontobee.org/ontology/CL](http://www.ontobee.org/ontology/CL)
    **The Cell Ontology is a structured controlled vocabulary for cell types in animals.**
    
* BTO [http://purl.obolibrary.org/obo/bto](http://purl.obolibrary.org/obo/bto)
    **A structured controlled vocabulary for the source of an enzyme 
    comprising tissues, cell lines, cell types and cell cultures**.
    
### What to do when there is no suitable ontology term.
Where there isn’t a term that is precisely right, consider using the ID for a 
term that is close enough, combined with text to say exactly what you mean. 
This will be marked with a warning at validation, but you can choose to ignore 
this.

You can also request a new term from the ontology. Guidance on this is below.

These approaches are not mutually exclusive – you could use a good 
approximation and update the records once a term has been created, as 
depending on the ontology it can take some time to be added.

### How to register a new ontology term.
Occasionally you will find that the existing ontology terms do not adequately 
cover the entity you are describing, this will be most likely to occur for the 
disease, cell type and breed ontologies.  In this situation you would need to 
register a new ontology term.  It is worth starting this process quickly as 
depending upon the ontology it can take time for it to be approved and 
included.  You will possibly require supporting information or literature 
references to confirm that the new term is real and must ensure that the term 
is not already described, please see [how to search for an ontology term](#how-to-search-for-an-existing-ontology-term).

Each ontology service has its own mechanism for the request of a new term and 
where an established process exists it will be briefly described below, 
we will endeavour to keep this list up to date so please contact us if you 
spot an error and for help and advice with any of these processes please 
contact [faang-dcc@ebi.ac.uk](mailto:faang-dcc@ebi.ac.uk)

If you would like assistance with registering a new term for any of the 
ontologies please contact [faang-dcc@ebi.ac.uk](mailto:faang-dcc@ebi.ac.uk)

###### Breed, trait and environment descriptions
**LBO** [http://bioportal.bioontology.org/ontologies/LBO](http://bioportal.bioontology.org/ontologies/LBO):

* Contact Cari Park, [caripark@iastate.edu](mailto:caripark@iastate.edu) with details of your required term.

**ATOL** [http://www.ebi.ac.uk/ols/beta/ontologies/atol](http://www.ebi.ac.uk/ols/beta/ontologies/atol)

* Request a username and password:
    * Send an email to [Pierre-Yves LeBail](mailto:Pierre-Yves.LeBail@rennes.inra.fr), [Pierre-Yves.LeBail@rennes.inra.fr](mailto:Pierre-Yves.LeBail@rennes.inra.fr) including:
    * Your name and organization / unit.
    * The ontology to which you wish to contribute (there may be several).
    * Your areas of interest and expertise.
    * Your species of interest as appropriate.
* You will receive a login / password and an address to connect to the Collaboration Server and follow these procedures.
* See [http://www.atol-ontology.com/rb/en/5](http://www.atol-ontology.com/rb/en/5) for more information (in french, Chrome can translate)

**EOL**[ http://www.ebi.ac.uk/ols/beta/ontologies/eol]( http://www.ebi.ac.uk/ols/beta/ontologies/eol)

* Request a username and password:
    * Send an email to [Pierre-Yves LeBail](mailto:Pierre-Yves.LeBail@rennes.inra.fr), [Pierre-Yves.LeBail@rennes.inra.fr](mailto:Pierre-Yves.LeBail@rennes.inra.fr) including:
    * Your name and organization / unit.
    * The ontology to which you wish to contribute (there may be several).
    * Your areas of interest and expertise.
    * Your species of interest as appropriate.
* You will receive a login / password and an address to connect to the Collaboration Server and follow these procedures.
* See [http://www.atol-ontology.com/rb/en/5](http://www.atol-ontology.com/rb/en/5) for more information (in french, Chrome can translate)

###### Disease
**EFO** [http://www.ebi.ac.uk/efo/](http://www.ebi.ac.uk/efo/)

* New terms are submitted through a JIRA ticketing system, a guide can be 
found at [http://www.ebi.ac.uk/efo/submit.html](http://www.ebi.ac.uk/efo/submit.html)

###### Other ontology resources
**NCBI Taxonomy** [http://www.ncbi.nlm.nih.gov/taxonomy](http://www.ncbi.nlm.nih.gov/taxonomy)

* It is unlikely that a species will not already be in the NCBI Taxonomy 
ontology, but please consult [http://www.ncbi.nlm.nih.gov/books/NBK21100/](
http://www.ncbi.nlm.nih.gov/books/NBK21100/) for further information and if 
you need to suggest a change in the existing classification please contact 
[info@ncbi.nlm.nih.gov](mailto:info@ncbi.nlm.nih.gov).

**VT** [http://bioportal.bioontology.org/ontologies/VT](http://bioportal.bioontology.org/ontologies/VT)

* Contact Jim Reecy, [jreecy@iastate.edu](mailto:jreecy@iastate.edu) with details of your required term.

**UBERON** [http://uberon.github.io/](http://uberon.github.io/)

* Submit a new Git issue [https://github.com/obophenotype/uberon/issues/new](https://github.com/obophenotype/uberon/issues/new)
* See [https://github.com/obophenotype/uberon/wiki/Editors-guide](https://github.com/obophenotype/uberon/wiki/Editors-guide)
* Contact Chris Mungall - cjmungall AT lbl DOT gov or Melissa Haendel - haendel AT ohsu DOT edu

**PATO** [http://purl.obolibrary.org/obo/pato](http://purl.obolibrary.org/obo/pato)

* Create a Git pull request on [https://github.com/pato-ontology/pato](https://github.com/pato-ontology/pato)
* See the guidelines at [https://github.com/pato-ontology/pato/blob/master/src/ontology/README-editors.md](https://github.com/pato-ontology/pato/blob/master/src/ontology/README-editors.md)
* For questions on this contact Chris Mungall  cjmungall AT lbl DOT gov or email obo-admin AT [obofoundry.org](http://obofoundry.org)

**CL** [http://www.ontobee.org/ontology/CL](http://www.ontobee.org/ontology/CL)

* [https://github.com/obophenotype/cell-ontology](https://github.com/obophenotype/cell-ontology)
* See [https://github.com/obophenotype/cell-ontology/blob/master/src/ontology/README-editors.txt](https://github.com/obophenotype/cell-ontology/blob/master/src/ontology/README-editors.txt)
* For more details on CL see: [http://obofoundry.org/ontology/cl.html](http://obofoundry.org/ontology/cl.html)
* For questions on this contact Chris Mungall  cjmungall AT lbl DOT gov

**OBI** [http://purl.obolibrary.org/obo/](http://purl.obolibrary.org/obo/)

* See [http://obi-ontology.org/page/Tutorials#Editing](http://obi-ontology.org/page/Tutorials#Editing)

**BTO** [http://purl.obolibrary.org/obo/bto](http://purl.obolibrary.org/obo/bto)

* Email[ a.chang@tu-bs.de](mailto:a.chang@tu-bs.de)
