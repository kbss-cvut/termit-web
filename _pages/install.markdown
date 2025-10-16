---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: single
title: Installation
permalink: /install
lang: en
lang-ref: install
classes: wide
author_profile: true
header:
  image: /assets/images/installation-header.jpg
  caption: "Photo credit: [**Clint Patterson**](https://unsplash.com/@cbpsc1?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText) on [**Unsplash**](http://unsplash.com/)"
---

The easiest way to run TermIt is with Docker Compose. The deployment takes care of all necessary services and
dependencies and does not require installation of any additional services or libraries.

The installation steps are described [here](https://github.com/kbss-cvut/termit-docker).

An alternative (more complicated) is to install and wire up the services independently. Follow individual installation
instructions for setting up each service:

- [TermIt Frontend](https://github.com/kbss-cvut/termit-ui)
- [TermIt Backend](https://github.com/kbss-cvut/termit)
