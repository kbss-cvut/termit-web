---
layout: single-cs
title: O TermItu
permalink: /cs/about
lang: cs
lang-ref: about
classes: wide
header:
  image: /assets/images/about-header.jpg
  caption: "Photo credit: [**Thom Holmes**](https://unsplash.com/@thomholmes?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText) on [**Unsplash**](http://unsplash.com/)"

feature_row:
  - image_path: /assets/images/about/deployment1.jpg
    alt: "Nasazení na IPR"
    title: "TermIt na IPR"
    excerpt: "Institut plánování a rozvoje hlavního města Prahy (IPR) používá TermIt od roku 2021. Systém TermIt byl vytvářen v projektu [OPPPR](https://www.penizeproprahu.cz/operacni-program-praha-pol-rustu-cr/) a IPR v rámci tohoto projektu testoval použitelnost TermItu k popisu Metropolitního plánu Prahy a jeho navázání na legislativní pojmy. Dnes je TermIt na IPR používán k systematizaci terminologií v dalších projektech, jako například Jednotný výměnný formát digitální technické mapy (JVF DTM) nebo Informační model budov (BIM)."
    btn_label: "Podívej se na TermIt na IPR"
    url: https://termit.fel.cvut.cz/ipr/#/public
    
feature_row2:
  - image_path: /assets/images/about/deployment3.jpeg
    alt: "TermIt na ČAS"
    title: "TermIt na ČAS"
    excerpt: "Česká agentura pro standardizaci používá TermIt v tuto chvíli pouze interně, ale v budoucnosti budou vytvořené slovníky zpřístupněny též veřejnosti."

feature_row3:
  - image_path: /assets/images/about/deployment2.jpg
    alt: "Nasazení v KODI"
    title: "TermIt nasazení v KODI"
    excerpt: "Ministerstvo vnitra České republiky zapracovao TermIt jako součást výrobní linky pro tvorby otevřených dat, včetně odpovídající dokumentace. TermIt slouží jako nástroj pro tvorbu glosářů legislativních slovníků. Ty jsou pak používány k anotaci datových sad a k vytváření propojení mezi legislativními dokumenty. Obsah tohoto nasazení zatím není veřejně přístupný."


feature_row4:
  - image_path: /assets/images/about/demo.png
    alt: "Živé demo"
    title: "Živé demo"
    excerpt: "Uživatelé si mohou vyzkoušet systém TermIt v demo verzi s omezeným přístupem. V demo verzi lze vyhledávat ve slovnících a pojmech a obsahuje mimo jiné Metropolitní plán Prahy, Stavební zákony České republiky a Nového Zélandu."
    btn_label: "Vyzkoušej demo"
    url: https://kbss.felk.cvut.cz/termit-demo/
---

<!-- # O TermItu -->

TermIt je systém pro správu slovníků a pojmů umožňující jejich propojování do legislatvních nebo jiných dokumentů a
dalších slovníků. Umožňuje vytvořit slovník pojmů obsažených v dokumentu, pevně definovat pojmy podle jejich významu a
pomocí funkčních vztahů je propojit s pojmy z jiných slovníků.

Motivací k tvorbě systému TermIt byla potřeba popsat pojmy používané různými skupinami expertů tak, aby si navzájem
rozuměly bez nutnosti učit se další názvosloví. Toho nebylo možné dosáhnout bez toho, aby se z doménových expertů stali
též experti ontologičtí. Nástroj TermIt umožňuje expertům na danou doménu vytvářet glosáře -- seznamy pojmů -- a
propojovat jejich pojmy s dalšími slovníky, ať už na úrovni jiné domény nebo nadřazené legislativy.

## Nasazení systému TermIt

TermIt je open-source projekt a jeho zdrojový kód lze nalézt na [GitHubu](https://github.com/kbss-cvut/termit). TermIt je v současnosti nasazen
v těchto organizacích:

{% include feature_row type="right"%}
{% include feature_row id="feature_row2" type="left"%}
{% include feature_row id="feature_row3" type="right"%}

[Nainstalujte si](/cs/install) a vyzkoušejte TermIt. Pokud vám chybí specifická funkcionalita, nebojte se nás
kontaktovat [e-mailem](mailto:petr.kremen@fel.cvut.cz), nebo nahlaště chyby či požadavky
v [tomto repozitáři](https://github.com/kbss-cvut/termit-ui). TermIt je modulární systém a můžeme ho nasadit v
podobě specifické pro Vaše potřeby.

## Živé demo

{% include feature_row id="feature_row4" type="left"%}

# Chci přispět

Pokud se chcete zůčastnit vývoje systému TermIt, forkněte si odpovídající repozítář:

- [Frontend](https://github.com/kbss-cvut/termit-ui)
- [Backend](https://github.com/kbss-cvut/termit)
- [Docker Compose nasazení](https://github.com/kbss-cvut/termit-docker)
  
a otevřete pull request.
