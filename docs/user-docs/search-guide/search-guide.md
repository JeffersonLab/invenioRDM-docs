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

## Combined simple, phrase or field search
Example: 
[<span style="color:#D13B1A;">+metadata.title:"open science" -metadata.title:policy</span>](https://jrdb.jlab.org/search?q=%2Bmetadata.title%3A%22open%20science%22%20-metadata.title%3Apolicy&l=list&p=1&s=10&sort=bestmatch) 

or e.g. [<span style="color:#D13B1A;">metadata.title:(-open +science)</span>](https://jrdb.jlab.org/search?q=metadata.title%3A%28-open%20%2Bscience%29&l=list&p=1&s=10&sort=bestmatch)

You can combine simple, phrase and field search to construct advanced search queries.


**More in [search guide](https://jrdb.jlab.org/help/search)**