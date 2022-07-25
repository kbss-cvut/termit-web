---
layout: single-cs
permalink: /cs/documentation
lang: cs
lang-ref: documentation
title: Dokumentace
#classes: wide
author_profile: true
header:
  image: /assets/images/documentation-header.jpg
  caption: "Photo credit: [**Joshua Hoehne**](https://unsplash.com/@mrthetrain?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText) on [**Unsplash**](http://unsplash.com/)"
toc: true
toc_sticky: true

---
<!-- # Dokumentace -->

V této sekci se postupně objeví dokumentace jednotlivých featur systému TermIt, seřazené podle abecedy.
<!-- filter only posts with category 'Documentation' and sort alphabeticaly by title-->

{% assign posts = site.categories.Dokumentace | sort: 'title' %}
{% for post in posts %}
  {% include documentation-single.html type=entries_layout %}
{% endfor %}
