---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: single
title: Technical Details
permalink: /technical-details
lang: en
lang-ref: technical-details
author_profile: true
header:
  image: /assets/images/data-model-header.jpg
  caption: "Photo credit: [**Toby56**](https://unsplash.com/@toby56?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText) on [**Unsplash**](http://unsplash.com/)"
toc: true
---

<!-- # Technical Details -->

This page contains some technical background of TermIt. It describes the architecture of the system, libraries developed
by us that it uses, and the data model at its core.

## Technologies and Architecture

Technically, TermIt is a system consisting of several services, one of them being a Web application called TermIt.
The application is split into two subprojects, one representing the backend (the
server side) and the other representing the frontend (the client side). The overall architecture of the TermIt system
can be seen in the following component diagram.

{% include figure image_path="/assets/images/technical-details/termit-architecture.png" alt="TermIt architecture
diagram" caption="TermIt architecture diagram" %}

Note that the diagram shows TermIt using a separate authentication service. TermIt can also be deployed with internal
authentication and user management.

### TermIt Backend

The backend is written in Java (17 or later). It is a [Spring Boot](https://spring.io/projects/spring-boot)-based Java
web application with a REST API supporting JSON and [JSON-LD](https://json-ld.org/). TermIt runs on top of a triple
store where it stores all its data. We use [GraphDB](https://graphdb.ontotext.com/) for its superior performance and
support
for custom inference rules which TermIt utilizes.

Details on how to configure or develop the TermIt backend can be found in
its [GitHub repository](https://github.com/kbss-cvut/termit).

### TermIt Frontend

The frontend is a client-side Web application written in TypeScript using the [React framework](https://reactjs.org/).
React is used for its simplicity of use and the vast ecosystem of libraries one can utilize.

The frontend source code can be found in its [GitHub repository](https://github.com/kbss-cvut/termit-ui), which also
contains some basic developer documentation.

### Annotace

One of the most interesting features of TermIt is its ability to analyze the content of documents to find
occurrences of terms and suggest new terms based on their
significance in the text. The text analysis functionality has been developed separately to enable its reuse.
This library is called **Annotace**, it is also open source and can be found
on [GitHub](https://github.com/kbss-cvut/annotace) as well.

### Validation

TermIt supports checking term quality using a set of [SHACL](https://www.w3.org/TR/shacl/) rules. Validation is provided
by a
separate [Validation service](https://github.com/kbss-cvut/validation-service).

### Notable Libraries

TermIt uses several custom libraries and components that may be of interest for other Semantic Web developers. Here is a
short list with some basic details and links with more details.

#### JOPA

[JOPA](https://github.com/kbss-cvut/jopa) (Java OWL Persistence API) is a persistence library for semantic data. It
allows working with a POJO-based domain model which is stored as RDF data in a triple store. Heavily inspired by JPA and
its implementation, JOPA contains all the necessary bells and whistles (transactions, query result mapping, caching) to
make development of a Semantic Web-based information system as smooth as possible.

There is also a [library](https://github.com/ledsoft/jopa-spring-transaction) for integrating JOPA with the declarative
transaction management of Spring (think `@Transactional`) that is used in TermIt.

#### JB4JSON-LD

[JB4JSON-LD](https://github.com/kbss-cvut/jb4jsonld) (Java Binding for JSON-LD) is a library for seamless marshalling
and unmarshalling of POJOs into and from JSON-LD. It integrates with Jackson, so the setup for an application is a
matter of just a couple of lines of code.

## Data Model

Vocabularies modeled in TermIt are compatible with [SKOS](https://www.w3.org/TR/skos-reference/). Two more ontologies
are used to cover additional parts of the data model: the Data description ontology and the TermIt ontology, both
developed by the Knowledge-based and Software Systems Group (KBSS).

### Data Description Ontology

Basic ontology used for description of any data. Its description as well as serialization in various RDF formats can be
found on [this page](https://onto.fel.cvut.cz/ontologies/slovnik/agendovy/popis-dat). It is based on the
Unified Foundational Ontology (UFO). The ontology allows describing any data source, such as databases, data in
various formats, files, etc.

The following paragraphs describe the basic classes defined in the model.

#### Vocabulary

Vocabulary represents an ontology, consists of glossary and model.

#### Glossary

Corresponding to SKOS ConceptScheme, a glossary is a list (a forest, when taking hierarchies into account) of all terms
present in vocabulary.

#### Model

A model brings ontological relations to the terms defined in the glossary, using mainly UFO.

#### Term

Corresponding to SKOS Concept, a term is any concept used in the vocabulary.

#### Source

Source represents the origin of data that are being modeled, e.g., database, data set, document, file, etc...

#### Attribute

Attribute is a special type of term, representing a property dependent on an object described in a source (e.g., a
column
in a database table, property described in a document, etc.).

### TermIt ontology

TermIt ontology has been created when developing TermIt. It inherits _Data description ontology_ and
extends it with concepts used specifically in an application such as TermIt.

Major problems solved by the TermIt ontology regard textual annotations, occurrences of terms in the sources and user
management.

The current version of the TermIt ontology is part of the TermIt source code and can be found
on [GitHub](https://github.com/kbss-cvut/termit/tree/master/ontology).
