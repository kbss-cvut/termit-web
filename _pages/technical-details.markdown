---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: single
# title: Technical Details
permalink: /technical-details
lang: en
lang-ref: technical-details
author_profile: true
header:
  image: /assets/images/data-model-header.jpg
  caption: "Photo credit: [**Toby56**](https://unsplash.com/@toby56?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText) on [**Unsplash**](http://unsplash.com/)"
toc: true
---

# Technical Details

This page contains some technical background of TermIt. It describes the architecture of the system, libraries developed by us that it uses, and the data model at its core.

## Technologies and Architecture

Technically, TermIt is a web application. The system is split into two sub-projects, one representing the backend and the other representing the frontend. The overall architecture of TermIt can be seen in the following component diagram.

{% include figure image_path="/assets/images/technical-details/termit-architecture.png" alt="TermIt architecture diagram" caption="TermIt architecture diagram" %}

### TermIt Backend

The backend is written in Java (8 or later). It is a [Spring Boot](https://spring.io/projects/spring-boot) -based Java web application with a REST API supporting JSON and [JSON-LD](https://json-ld.org/). TermIt runs on top of a triple store where it stores all its data. It has been tested with [RDF4J](https://rdf4j.org/) and [GraphDB](https://graphdb.ontotext.com/) with GraphDB delivering more favorable performance.

Details on how to configure or develop the TermIt backend can be found in its [GitHub repository](https://github.com/kbss-cvut/termit).


### TermIt Frontend

The frontend is a client-side web application written in TypeScript using the [React framework](https://reactjs.org/). React is used for its simplicity of use and the vast ecosystem of libraries one can utilize.

The frontend source code can be found in its [GitHub repository](https://github.com/kbss-cvut/termit-ui), which also contains some basic developer documentation.

### Integration with Annotace

One of the most interesting features of TermIt is its ability to analyze content of document in order to find occurrences of terms and suggest new terms based on their
significance in the text. The text analysis functionality has been developed separately to enable its reuse.
This library is called **Annotace**, it is open source and can be found on [GitHub](https://github.com/kbss-cvut/annotace) as well.


### Notable Libraries

TermIt uses several custom libraries and components that may be of interest for other Semantic Web developers. Here is a short list with some basic details
and links with more details.

#### JOPA

[JOPA](https://github.com/kbss-cvut/jopa) (Java OWL Persistence API) is a persistence library for semantic data. It allows working with POJO-based domain model which is stored as RDF data in a triple store. Heavily inspired by JPA and its implementation, JOPA contains all the necessary bells and whistles (transactions, query result mapping, caching) to make development
of a Semantic Web-based information system as smooth as possible.

There is also a [library](https://github.com/ledsoft/jopa-spring-transaction) for integrating JOPA with the declarative transaction management of Spring (think `@Transactional`) that is used in TermIt.

#### JB4JSON-LD
[JB4JSON-LD](https://github.com/kbss-cvut/jb4jsonld) (Java Binding for JSON-LD) is a library for seamless marshalling and unmarshalling of POJOs into and from JSON-LD. It integrates with Jackson, so the set-up for an application is a matter of just a couple of lines of code.

## Data Model

Vocabularies modelled in TermIt are using two specific data models -- Data description ontology and TermIt ontology, both developed by Knowledge-based and Software Systems Group (KBSS).

### Data description ontology

Basic ontology used for description of any data is called Data description ontology and is described on [this page](http://onto.fel.cvut.cz/ontologies/slovnik/agendovy/popis-dat/current/index-en.html). It is based on the Unified Foundational Ontology (UFO). The ontology is made to describe any data source, such as databases, data in various formats, files etc.

The current version of Data description ontology can be found [here](https://onto.fel.cvut.cz/ontologies/page/slovnik/agendovy/popis-dat/model/verze/1.0.1) in turtle or RDF/XML.

Following sections describes basic classes defined in the model.

#### Vocabulary
Vocabulary represents an ontology, consists of glossary and model.

#### Glossary
Glossary is a list of all terms present in vocabulary, using only skos concepts.

#### Model
Model brings ontological relations to the terms defined in the glossary, using mainly UFO.

#### Term
Term is any concept used in the vocabulary.

#### Source
Source represents the origin of data that are being modelled, e.g. database, data set, document, file etc...

#### Attribute
Attribute is a special type of term, representing a property dependent on an object described in a source (e.g. a column in a database table, property described in a document etc.).

### TermIt ontology

TermIt ontology has been created while developing TermIt software. It inherits common Data description ontology and extends it for the concepts used specifically in TermIt.

Major problems solved by the TermIt ontology regard textual annotations, occurrences of terms in the sources and user management.

Current version of TermIt ontology is part of the TermIt deployment and can be accessed from [GitHub](https://github.com/kbss-cvut/termit/tree/master/ontology).
