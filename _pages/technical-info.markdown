---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: single
#title: Technical information
permalink: /technical-info
header:
  image: /assets/images/data-model-header.jpg
  caption: "Photo credit: [**Toby56**](https://unsplash.com/@toby56?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText) on [**Unsplash**](http://unsplash.com/)"
---

TermIt is an information system with a strong formal background. This page contains some technical background of TermIt. 
It describes the architecture of the system, interesting technologies it uses, and the data model at its core.


# Technologies and Architecture

## Overview

Technically, TermIt is a Web application. The system is split into two sub-projects, one representing the backend and the other representing the frontend.

### TermIt Backend

The backend is written in Java (8 or later). It is a [Spring Boot](https://spring.io/projects/spring-boot) -based Java Web application with a REST API 
supporting JSON and [JSON-LD](https://json-ld.org/). TermIt runs on top of a triple store where it stores all its data. We have used 
[RDF4J](https://rdf4j.org/) and [GraphDB](https://graphdb.ontotext.com/) with GraphDB delivering more favorable performance.

Details on how to configure or develop the TermIt backend can be found in its [GitHub repository](https://github.com/kbss-cvut/termit).


### TermIt Frontend

The frontend is a client-side Web application written in TypeScript using the [React framework](https://reactjs.org/). We have used React for its simplicity of use,
and the vast ecosystem of libraries one can utilize.

The frontend source code can be found in its [GitHub repository](https://github.com/kbss-cvut/termit-ui), which also contains some basic developer documentation.

### Annotace

One of the more interesting features of TermIt is its ability to analyze content of document in order to find occurrences of terms and suggest new terms based on their
significance in the text. Our goal in this regard was to not create a monolith. Instead, the text analysis functionality has been developed separately to enable its
reuse. This library is called **Annotace**, it is open source and can be found on [GitHub](https://github.com/kbss-cvut/annotace) as well.


## Interesting Libraries

TermIt uses several custom libraries and components that may be of interest for other Semantic Web developers. Here is a short list with some basic details 
and links where you can find more.

# Data Model

