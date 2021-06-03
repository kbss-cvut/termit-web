---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: single-cs
title: Nasazení
permalink: /cs/deployments
lang: cs
lang-ref: deployments
classes: wide
header:
  image: /assets/images/deployments-header.jpg
  caption: "Photo credit: [**Clint Patterson**](https://unsplash.com/@cbpsc1?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText) on [**Unsplash**](http://unsplash.com/)"

feature_row:
  - image_path: /assets/images/deployments/deployment1.jpg
    alt: "Nasazení prvního deploymentu"
    title: "First deployment"
    excerpt: "Total description of running deployment on IPR."
    btn_label: "Click here to see it"
    url: /link-na-ipr

feature_row2:
  - image_path: /assets/images/deployments/deployment2.jpg
    alt: "Nasazení druhého deploymentu"
    title: "Second deployment"
    excerpt: "Total description of running deployment in KODI."
    btn_label: "Click here to see it"
    url: /link-na-kodi
---
# Running deployments
This page displays current deployments.

TermIt is partly modular system and we can deploy it specifically for your needs.

{% include feature_row type="right"%}
{% include feature_row id="feature_row2" type="left"%}
