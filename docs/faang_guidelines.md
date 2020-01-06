# FAANG guidelines for livestock breed nomenclature
The FAANG sample metadata specification requires that the breed of each animal 
is documented, using terms from the [Livestock Breed Ontology](https://bioportal.bioontology.org/ontologies/LBO) (LBO). This 
document covers how to describe the breed of animals. 

### Purebred animals
Purebred animals should be described using a single term from LBO. The breed 
name should be used as the value, with a reference to the ontology ID. e.g an 
entry using the FAANG metadata template would look like this for a Texel sheep:

breed | Term Source ID 
------------ | ------------- 
Texel | LBO_0000640

### Crossbred animals
All crossbred animals should be annotated with the LBO term ID for crossbreed, 
specific to their species.

Species | Term Source ID 
------------ | ------------- 
Bos taurus | LBO_0001036
Capra hircus | LBO_0001038
Equus caballus | LBO_0001039
Gallus gallus | LBO_0001037
Ovis aries | LBO_0001041
Sus scrofa | LBO_0001040

### Cross of two pure bred animals
Where the breed of the parent animals are known, the progeny of two purebred 
animals can be described using the format “breed sire x breed dam”. Sire should 
always be listed first, dam second. For example

breed | Term Source ID 
------------ | ------------- 
Texel sire x Scottish Blackface dam | LBO_0001041
Scottish Blackface sire x Texel dam | LBO_0001041

### Breed of each parent is not known
Where the details of the breeding line are not fully known, the breed should 
be reported as a list of breed names, separated by a comma. The breeds should 
be ordered alphabetically. For example,  the progeny of a Texel and Scottish 
Blackface cross:

breed | Term Source ID 
------------ | ------------- 
Scottish Black,Texel | LBO_0001041

### Cross of a crossbreed and a purebred animal
Where a crossbreed is bred with a purebred animal (e.g. a backcross), breed 
information can be nested, following the same ordering as for outcrossed 
animals (sire first).

breed | Term Source ID 
------------ | ------------- 
(Texel sire x Scottish Blackface dam) sire x Texel dam | LBO_0001041
Texel sire x (Texel sire x Scottish Blackface dam) dam | LBO_0001041

### Cross of two crossbred animals and further crosses
There are practical limits to how much information can be stored in a single 
field. Full details of a breeding line can be represented by submitting 
information about the animals, and linking the records using the ‘Child of’ 
relationship in the animal metadata. In these cases, breed can be summarised 
following the same rules as for animals where we do not know the breed of each 
parent.

In the example below, we know enough of the S5’s lineage to describe it as 
“(Texel sire x Scottish Blackface dam) sire x (Texel sire x Scottish Blackface 
dam) dam”, but this is unwieldy, so we summarise it as “Scottish Blackface;Texel”.

Animal | Child of | Child of | breed | Term Source ID
------------ | ------------- | ------------- | ------------- | -------------
S1 | | | Texel | LBO_0000640
S2 | | | Scottish Blackface | LBO_0000612
S3 | S1 | S2 | Texel sire  x Scottish Blackface dam | LBO_0001041
S4 | S1 | S2 | Texel sire  x Scottish Blackface dam | LBO_0001041
S5 | S3 | S4 | Scottish Blackface,Texel | LBO_0001041
