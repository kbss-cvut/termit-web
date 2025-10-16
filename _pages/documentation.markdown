---
layout: single
permalink: /documentation
lang: en
title: Documentation
lang-ref: documentation
#classes: wide
author_profile: true
header:
  image: /assets/images/documentation-header.jpg
  caption: "Photo credit: [**Joshua Hoehne**](https://unsplash.com/@mrthetrain?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText) on [**Unsplash**](http://unsplash.com/)"
toc: true
toc_sticky: true

---
<!-- # Documentation -->

This section contains the list of features supported by TermIt.

## Glossary Management

- Creating, editing, and viewing glossaries
    - A glossary has a configurable primary language, which determines the language required for concept names
    - Linking related glossaries
- Creating, editing, and viewing concepts
    - Concept properties follow the [SKOS](https://www.w3.org/TR/skos-reference/) standard
    - Concept hierarchies can be created even across linked glossaries
    - Ability to view and edit properties beyond the base application model
    - Classification of concepts according to a configurable taxonomy
- Multilingual concepts and glossaries
    - Each concept and glossary can have translations of relevant properties in any language
    - A translation in the glossary’s primary language is mandatory
- Recording the history of changes to glossaries and concepts, including the author of each change
- Access control for glossaries at the level of roles, user groups, and individual users
- Creating and viewing glossary snapshots (including all concepts and related glossaries)
    - Snapshots are read-only and serve to record the state of a glossary at a given point in time
- Commenting on concepts and rating comments (thumbs up or down)
- Managing the concept life cycle using states
- Defining new properties for glossaries and concepts
- Concept quality validation
    - Using [SHACL](https://www.w3.org/TR/shacl/) rules
- Full-text search of concepts and glossaries
    - Including the option to select the search language
- Faceted search of concepts
- Importing a glossary from a file containing RDF compatible with SKOS
- Importing translations of existing concepts from a file containing RDF compatible with SKOS
- Importing a glossary from an MS Excel file
- Importing a glossary from a configurable external source
    - The external source is a SPARQL endpoint containing SKOS-compatible data
    - TermIt ensures continuous automatic synchronization of the external glossary (every 24 hours)
- Exporting a glossary to a file containing RDF compatible with SKOS
- Exporting a glossary to an MS Excel file
- Use of Markdown formatting in relevant attributes (e.g., concept definitions)
- Meaningful identifiers generated from the name
    - Based on the primary language
    - The generated identifier can be manually changed (when creating a concept or glossary)

## Document and Text Annotation

- Each glossary can be associated with a set of documents
- Documents can be uploaded into the system; HTML is supported
- [Text analysis service](https://github.com/kbss-cvut/annotace)
    - Finding occurrences of existing concepts in text
    - Suggesting new concepts based on their importance in the text
    - Semi-automatic - the user must confirm occurrences
- Linking a concept definition to a specific location in a document
- Reusing confirmed occurrences when uploading a new version of a document
- Suggesting related concepts (within the glossary) based on analysis of the concept definition

## Other Features

- User authorization based on roles (+ access control via access lists, see above)
- Registration/password reset via email link
- Integration with an authentication service (standard OAuth2/OIDC)
    - User management is then handled by this service
- Public user interface for viewing glossaries and concepts
    - Can be disabled
- REST API with documentation compliant with the [OpenAPI](https://www.openapis.org/) standard
- Dashboard overview of recently changed and commented concepts
- Basic statistics
    - Number of concepts/glossaries/users
    - Distribution of concept counts among glossaries
    - Distribution of concept classifications
    - User activity within a glossary (new concepts/edits/deletions)
- Localization of the user interface into English and Czech
- Optional regular weekly email overview of activity (changes, comments)
