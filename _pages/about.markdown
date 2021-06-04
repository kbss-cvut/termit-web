---
layout: single
# title: About
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
    alt: "Deployment on IPR"
    title: "TermIt deployment on IPR"
    excerpt: "TermIt runs on IPR since 2020. It was originally used to describe Metropolitan plan and help to relate it to the legislation. The main problem to solve is that experts from different domains uses different terminology, and all of them must contribute. Nowadays, TermIt serves as an intermediary for many other projects besides Metropolitan plan."
    btn_label: "See TermIt on IPR"
    url: https://termit.fel.cvut.cz/ipr/#/public

feature_row2:
  - image_path: /assets/images/about/deployment2.jpg
    alt: "Deployment in KODI"
    title: "TermIt deployment in KODI"
    excerpt: "Ministry oif interior of the Czech Republic incorporated TermIt as a part of the production line for creation of open data, including proper documentation. TermIt serves as a tool for creation of legislation glossaries. They are used to annotate data sets and create interlinks between legislation."
    btn_label: "Click here to see it"
    url: http://slovník.gov.cz/modelujeme

feature_row3:
  - image_path: /assets/images/about/demo.png
    alt: "Live demo"
    title: "Live demo"
    excerpt: "Users may try live demo of system TermIt with limited permissions to browse vocabularies and terms, e.g. Metropolitan plan, Building laws of the Czech Republic and New Zealand and others."
    btn_label: "Try live demo"
    url: https://kbss.felk.cvut.cz/termit-demo/
---

# About TermIt

TermIt is a system for management of terms and vocabularies and their interconnection to legislation (or other documents) and other vocabularies.

It was created originally for Institute of planning and development (IPR) of Prague. People from IPR needed to describe terms used by different group of specialists. Without being the ontology expert, it was impossible fot them to make it. The tool helps domain experts to create ontological glossaries.

## Deployments

TermIt is an open-source project. The core version is available from [TermItGitHub](https://github.com/kbss-cvut/termit). For specific customers were created few specific versions. TermIt is already running in following deployments:

{% include feature_row type="right"%}
{% include feature_row id="feature_row2" type="left"%}

[Install](/install) and try  core version. Feel free to [contact us](mailto:petr.kremen@fel.cvut.cz), if there is something missing. TermIt is partly modular system and we can deploy it specifically for Your needs.

## Live demo

{% include feature_row id="feature_row3" type="right"%}


# Contributing

Do You want to contribute? Feel free to fork the respective repository:
- [frontend](https://github.com/kbss-cvut/termit-ui)
- [backend](https://github.com/kbss-cvut/termit)
- [docker instrumentation](https://github.com/kbss-cvut/termit-docker)
and open a pull request with Your contribution.
