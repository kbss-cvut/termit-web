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

In this section, the documentation of individual features of TermIt will gradually appear, sorted alphabetically.

<!-- V této sekci se postupně objeví dokumentace jednotlivých featur systému TermIt, seřazené podle abecedy. -->
<!-- filter only posts with category 'Documentation' and sort alphabeticaly by title-->

{% assign posts = site.categories.Documentation | sort: 'title' %}
{% for post in posts %}
  {% include documentation-single.html type=entries_layout %}
{% endfor %}
