This guide explains how to write advanced search queries using easy to understand examples.

## Simple search (one or multiple terms)
Example: [<span style="color:#D13B1A;">open science</span>](https://jrdb.jlab.org/search?q=open%20science&l=list&p=1&s=10&sort=bestmatch)

Results will match records with the terms open or science in any field. Note that stemming is applied so e.g. science will also match sciences. Search results are ranked according to an algorithm that takes your query terms into account.

You can require presence of both terms using either the + or AND operator:

Examples: [<span style="color:#D13B1A;">open AND science</span>](https://jrdb.jlab.org/search?q=open%20AND%20science&l=list&p=1&s=10&sort=bestmatch) or [<span style="color:#D13B1A;">+open +science</span>](https://jrdb.jlab.org/search?q=%2Bopen%20%2Bscience&l=list&p=1&s=10&sort=bestmatch)

You can require absence of one or more terms using either the - or NOT operator:

## Phrase search
Example: [<span style="color:#D13B1A;">"open science"</span>](https://jrdb.jlab.org/search?q=%22open%20science%22&l=list&p=1&s=10&sort=bestmatch)

Results will match records with the phrase open science in any field.

## Field search
Example: [<span style="color:#D13B1A;">metadata.title:open</span>](https://jrdb.jlab.org/search?q=metadata.title%3Aopen&l=list&p=1&s=10&sort=bestmatch)

Results will match records with the term open in the field metadata.title. If you want to search for multiple terms in the title you must group the terms using parenthesis:

Example: [<span style="color:#D13B1A;">metadata.title:(open science)</span>](https://jrdb.jlab.org/search?q=metadata.title%3A%28open%20science%29&l=list&p=1&s=10&sort=bestmatch)

see [**Metadata List**](../../metadata/index.md) for the full list of fields you can search.

### Search records via experiment number
Example: 
[<span style="color:#D13B1A;">custom_fields.rdm\:experiment_number:"E93-006"</span>](https://jrdb.jlab.org/search?q=custom_fields.rdm%5C%3Aexperiment_number%3A%22E93-006%22&l=list&p=1&s=10&sort=bestmatch)

you will get all the record that has exact match to experiment number "E93-006"

### Search records via pac number
Example:
[<span style="color:#D13B1A;">custom_fields.pac\:pac_number:50</span>](https://jrdb.jlab.org/search?q=custom_fields.pac%5C%3Apac_number%3A50&l=list&p=1&s=10&sort=bestmatch)

You will get all the record that has exact match to pac_number 50.

### Search records via proposal number 
[<span style="color:#D13B1A;">custom_fields.pac\:proposal_number:"E12-10-006"</span>](https://jrdb.jlab.org/communities/pacdb/records?q=custom_fields.pac%5C%3Aproposal_number%3A%22E12-10-006%22&l=list&p=1&s=10&sort=bestmatch)

you will get a single record that has exact match to the proposal number "E12-10-006"

### Search for all record across publicationDb and pacDB
If you want get all documents across different DB, for experiment number "E12-13-005", just get the only the number i.e. "1213005". Then search as:

[<span style="color:#D13B1A;">custom_fields.rdm\:expID:1213005</span>](https://inveniordm.jlab.org/search?q=custom_fields.rdm%5C%3AexpID%3A1213005&l=list&p=1&s=10&sort=bestmatch)

You will get document across with experiment number "E12-13-005" and proposal number "12-13-005".

### Search for all LDRD documents
Example:
[<span style="color:#D13B1A;">custom_fields.rdm\:isldrd:true</span>](https://jrdb.jlab.org/search?q=custom_fields.rdm%5C%3Aisldrd%3Atrue&l=list&p=1&s=10&sort=bestmatch)|

You will get all documents related to LDRD.

### search by LDRD number
Example:
[<span style="color:#D13B1A;">custom_fields.rdm\:ldrd_number:2024-LDRD-2</span>](https://jrdb.jlab.org/search?q=custom_fields.rdm%5C%3Aldrd_number%3A2024-LDRD-2&l=list&p=1&s=10&sort=bestmatch)

You will get all documents related to LDRD number "2024-LDRD-2"

## Combined simple, phrase or field search
Example: 
[<span style="color:#D13B1A;">+metadata.title:"open science" -metadata.title:policy</span>](https://jrdb.jlab.org/search?q=%2Bmetadata.title%3A%22open%20science%22%20-metadata.title%3Apolicy&l=list&p=1&s=10&sort=bestmatch) 

or e.g. [<span style="color:#D13B1A;">metadata.title:(-open +science)</span>](https://jrdb.jlab.org/search?q=metadata.title%3A%28-open%20%2Bscience%29&l=list&p=1&s=10&sort=bestmatch)

You can combine simple, phrase and field search to construct advanced search queries.


**More in [search guide](https://jrdb.jlab.org/help/search)**



## 