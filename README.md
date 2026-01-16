# Eduard Jurášek - Internet slang vocabulary (topic 5)

The proposed seminar project aims to implement graph database of the contemporary
Internet slang vocabulary represented in RDF. By internet slang, I refer words, phrases or
acronyms frequently used online and/or in casual speech as well.

These words have complex relationships and linguistic backstories. The graph database
is planned not only as a “word” – “meaning” principle, but include:
-Definition
-Origin
-Example in sentence
-Community usage

Over 120 words are covered in .ttl

The Definition and the Example in Sentence were used from https://www.urbandictionary.com/. Some parts were edited or censored.

The project was inspired by a masters thesis of a friend of mine. Thank you so much, Jakub!

Riecky, J. (2025). Internet vernacular - a study of neologisms in online discourse of cybercultures [Masters Thehis, Univerzita sv. Cyrila a Metoda v Trnave FF UCM KAA]. Centrálny register záverečných a kvalifikačných prác OPAC CRZP. https://opac.crzp.sk/?fn=detailBiblioFormChildM8GSN&sid=6F9F3F51667F0CBC3D41BFEE069E&seo=CRZP-detail-kniha 

For finding the creation dates and goups of origin, GPT-5 in a Deep Research mode was used for some parts I struggled to find manually.

This project aims to make a Urban Dictionary - like database represented as a graph, but with additional perks mentioned above.
A real-world usage is to make a web UI layer and plot the results in an appealing form directly in a web browser (not yet implemented).

The development was made in a VSCode, Protege and Fuseki on a Kubuntu Linux.

---
## Using already existing ontologies

@prefix skos:   <http://www.w3.org/2004/02/skos/core#> . Used to create a backbone - concept, definition, example. 

@prefix foaf:   <http://xmlns.com/foaf/0.1/> . Used to state who is responsible for the creation of the word

@prefix dcterms:<http://purl.org/dc/terms/> . Used to state when was the word created

@prefix dbr:    <http://dbpedia.org/resource/> . Used to assign a link to DBPedia where more information about the topic can be found if someone is not familiar in the field.

@prefix xsd:    <http://www.w3.org/2001/XMLSchema#> . Used to assign years as a date format using ^^xsd:gYear.

---
## Using own ontology

I named this ontology as ISV - Internet Slang Vocabulary.

@prefix isv:    <https://github.com/ejurasek00/isv/#> . (Custom) – Used to define the specific class isv:SlangTerm and project metadata. Subclass of skos:Concept

---
Having any questions or suggestions on how to make this project better, do not hesitate
to contact me via E-mail jure01@vse.cz
