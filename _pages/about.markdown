---
layout: single
title: About TermIt
permalink: /about
lang: en
lang-ref: about
classes: wide
author_profile: true
header:
  image: /assets/images/about-header.jpg
  caption: "Photo credit: [**Thom Holmes**](https://unsplash.com/@thomholmes?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText) on [**Unsplash**](http://unsplash.com/)"

feature_row:
  - image_path: /assets/images/about/deployment1.jpg
    alt: "TermIt at IPR"
    title: "TermIt at IPR"
    excerpt: "TermIt has been used by the Institute of Planning and Development of Prague (IPR) since 2021. TermIt was originally created in a [OPPPR project](https://www.penizeproprahu.cz/operacni-program-praha-pol-rustu-cr/) and IPR tested its usability -- to describe the Metropolitan plan and help to relate it to the legislation. Nowadays, TermIt serves for systemization of terminology in other areas, e.g., Uniform Interchangeable Format of the Digital Technical Map (JVF DTM) and Building Intelligence Model (BIM)."
    btn_label: "See TermIt on IPR"
    url: https://termit.fel.cvut.cz/ipr/#/public
    
feature_row2:
  - image_path: /assets/images/about/deployment3.jpeg
    alt: "TermIt at CAS"
    title: "TermIt at CAS"
    excerpt: "TermIt has been used by the Czech Standardization Agency (CAS). Currently only used internally, the results of its use are planned to be published in the future."

feature_row3:
  - image_path: /assets/images/about/deployment2.jpg
    alt: "Deployment in KODI"
    title: "TermIt deployment in KODI"
    excerpt: "The Ministry of interior of the Czech Republic incorporated TermIt as a part of the assembly line for creation of open data, including proper documentation. TermIt serves as a tool for creation of legislation glossaries. They are used to annotate data sets and create interlinks between legislation. The resulting data are accessible in the [Semantic Vocabulary](https://datagov-cz.github.io/ssp/)."


feature_row4:
  - image_path: /assets/images/about/demo.png
    alt: "Live demo"
    title: "Live demo"
    excerpt: "You can try a live demo of TermIt with limited permissions to browse vocabularies and terms, e.g. Metropolitan plan, Building laws of the Czech Republic and New Zealand and others."
    btn_label: "Try live demo"
    url: https://kbss.felk.cvut.cz/termit-demo/
---

<!-- # About TermIt -->

TermIt is a system for managing terms and vocabularies and their interconnection to legislation (or other documents) and
other vocabularies.

Motivation to create such a system originated in a need to describe terms used by different groups of experts to make
them understand each other without a need to learn new terminology. Without being an ontology expert, it was impossible
to achieve the aforementioned goal. The tool helps domain experts to create ontological glossaries and interconnect
their terms to other vocabularies.

## Deployments

TermIt is an open-source project. Its source code can be found on [GitHub](https://github.com/kbss-cvut/termit). TermIt is already running in the following deployments:

{% include feature_row type="right"%}
{% include feature_row id="feature_row2" type="left"%}
{% include feature_row id="feature_row3" type="right"%}

[Install](/install) it and try. Feel free to [contact us](mailto:petr.kremen@fel.cvut.cz) if there is
something missing, or report an issue in [this repository](https://github.com/kbss-cvut/termit-ui). TermIt is a
modular system, and we can deploy it specifically for Your needs.

## Live demo

{% include feature_row id="feature_row4" type="left"%}

# Contributing

Do You want to contribute? Feel free to fork the respective repository:

- [Frontend](https://github.com/kbss-cvut/termit-ui)
- [Backend](https://github.com/kbss-cvut/termit)
- [Docker Compose configuration](https://github.com/kbss-cvut/termit-docker)

and open a pull request with Your contribution.
