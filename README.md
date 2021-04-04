# TermIt web

Web theme is based on the [Minimal Mistakes Jekyll theme](https://mmistakes.github.io/minimal-mistakes/) under the MIT License, using Jekyll.

[![LICENSE](https://img.shields.io/badge/license-MIT-lightgrey.svg)](https://raw.githubusercontent.com/mmistakes/minimal-mistakes/master/LICENSE)
[![Jekyll](https://img.shields.io/badge/jekyll-%3E%3D%203.7-blue.svg)](https://jekyllrb.com/)

Web describes the basic features of TermIt and basic information about its authors. It contains following sections:

- About - Basic information about,
- Install - step-by-step installation process,
- Tutorial - description of the basic usage scenarios,
- Deployments - description and links to current deployments,
- Data model - description of existing data models.



## Changes
Current state of TermIt web is basically without content. Is is necessary to follow some rules during the content creation.

- Create new branch to push changes.
- For each section is created a .md file in [_pages][_pages]. Feel free to create any content, but do not change the header (between --- lines).
- Locate images used in every section in the designated folder in [assets/images][assets/images].

For including images use:
```
{% include figure image_path="/assets/images/image.jpg" alt="this is a placeholder image" caption="This is a figure caption." %}
```

**Do not change anything else than content of [_pages][_pages] and [assets/images][assets/images]**
