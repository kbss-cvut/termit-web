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

This page contains some technical background of TermIt. It describes the architecture of the system, libraries developed by us that it uses, and the data model at its core.


# Technologies and Architecture

## Overview

Technically, TermIt is a web application. The system is split into two sub-projects, one representing the backend and the other representing the frontend. The overall
architecture of TermIt can be seen in the following component diagram.
{% include figure image_path="/assets/images/technical-details/termit-architecture.png" alt="TermIt architecture diagram" caption="TermIt architecture diagram" %}

### TermIt Backend

The backend is written in Java (8 or later). It is a [Spring Boot](https://spring.io/projects/spring-boot) -based Java web application with a REST API
supporting JSON and [JSON-LD](https://json-ld.org/). TermIt runs on top of a triple store where it stores all its data. It has been tested with
[RDF4J](https://rdf4j.org/) and [GraphDB](https://graphdb.ontotext.com/) with GraphDB delivering more favorable performance.

Details on how to configure or develop the TermIt backend can be found in its [GitHub repository](https://github.com/kbss-cvut/termit).


### TermIt Frontend

The frontend is a client-side web application written in TypeScript using the [React framework](https://reactjs.org/). React is used for its simplicity of use
and the vast ecosystem of libraries one can utilize.

The frontend source code can be found in its [GitHub repository](https://github.com/kbss-cvut/termit-ui), which also contains some basic developer documentation.

### Integration with Annotace

One of the more interesting features of TermIt is its ability to analyze content of document in order to find occurrences of terms and suggest new terms based on their
significance in the text. The text analysis functionality has been developed separately to enable its reuse.
This library is called **Annotace**, it is open source and can be found on [GitHub](https://github.com/kbss-cvut/annotace) as well.


## Notable Libraries

TermIt uses several custom libraries and components that may be of interest for other Semantic Web developers. Here is a short list with some basic details
and links with more details.

#### JOPA

[JOPA](https://github.com/kbss-cvut/jopa) (Java OWL Persistence API) is a persistence library for semantic data.
It allows working with POJO-based domain model which is stored as RDF data in a triple store.
Heavily inspired by JPA and its implementation, JOPA contains all the necessary bells and whistles (transactions, query result mapping, caching) to make development
of a Semantic Web-based information system as smooth as possible.

There is also a [library](https://github.com/ledsoft/jopa-spring-transaction) for integrating JOPA with the declarative
transaction management of Spring (think `@Transactional`) that is used in TermIt.

#### JB4JSON-LD
[JB4JSON-LD](https://github.com/kbss-cvut/jb4jsonld) (Java Binding for JSON-LD) is a library for seamless marshalling and unmarshalling of POJOs into and from JSON-LD.
It integrates with Jackson, so the set-up for an application is a matter of just a couple of lines of code.


# Data Model
