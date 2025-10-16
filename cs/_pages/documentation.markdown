---
layout: single-cs
permalink: /cs/dokumentace
lang: cs
lang-ref: dokumentace
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

Tato sekce obsahuje seznam všech funkcí systému TermIt.

## Správa slovníků

- Vytváření, editace, prohlížení slovníků
  - Slovník má nastavitelný primární jazyk, který určuje, v jakém jazyce jsou vyžadovány názvy pojmů
  - Propojení souvisejících slovníků
- Vytváření, editace, prohlížení pojmů
  - Vlastnosti pojmů odpovídají standardu [SKOS](https://www.w3.org/TR/skos-reference/)
  - Hierarchii pojmů lze vytvářet i napříč propojenými slovníky
  - Možnost prohlížet a editovat vlastnosti nad rámec základního modelu aplikace
  - Klasifikace pojmů dle nastavitelné taxonomie
- Vícejazyčné pojmy a slovníky
  - Každý pojem i slovník může mít překlady relevantních vlastností v libovolném jazyce
  - Povinný je překlad v primárním jazyce slovníku
- Zaznamenávání historie změn slovníků i pojmů, včetně autora změny
- Řízení přístupu ke slovníkům na úrovni rolí, uživatelských skupin a jednotlivých uživatelů
- Vytváření a prohlížení snapshotů slovníků (včetně všech pojmů a souvisejících slovníků)
  - Snapshoty jsou pouze ke čtení a slouží k zaznamenání stavu slovníku v daném časovém okamžiku
- Komentování pojmů a hodnocení komentářů (palec nahoru či dolů)
- Řízení životního cyklu pojmu pomocí stavů
- Definice nových vlastností pro slovníky i pojmy
- Validace kvality pojmu
  - Za použití [SHACL](https://www.w3.org/TR/shacl/) pravidel
- Fulltextové vyhledávání pojmů a slovníků
  - Včetně možnosti vybrat jazyk vyhledávání
- Fasetové vyhledávání pojmů
- Import slovníku ze souboru obsahujícího RDF kompatibilní se SKOS
- Import překladů existujících pojmů ze souboru obsahujícího RDF kompatibilní se SKOS
- Import slovníku ze souboru MS Excel
- Import slovníku z konfigurovatelného externího zdroje
  - Externím zdrojem je SPARQL endpoint obsahující data kompatibilní se SKOS
  - TermIt zajišťuje průběžnou automatickou synchronizaci externího slovníku (každých 24h)
- Export slovníku do souboru obsahujícího RDF kompatibilní se SKOS
- Export slovníku do souboru MS Excel
- Použití Markdown formátování v relevantních atributech (např. definice pojmu)
- Smysluplné identifikátory generované z názvu
  - Na základě primárního jazyka
  - Generovaný identifikátor lze ručně změnit (při vytváření pojmu/slovníku) 

## Anotace dokumentů a dalších textů

- Ke každému slovníku lze přiřadit množinu dokumentů
- Dokumenty lze nahrát do systému, podporován je formát HTML
- [Služba textového analýzy](https://github.com/kbss-cvut/annotace)
  - Vyhledávání výskytů existujících pojmů v textu
  - Návrh nových pojmů na základě jejich důležitosti v textu
  - Uživatel výskyty musí potvrdit
- Propojení definice pojmu s konkrétním místem v dokumentu
- Přepoužití potvrzených výskytů při nahrání nové verze dokumentu
- Návrh souvisejících pojmů (v rámci slovníku) na základě analýzy textu definice pojmu

## Další funkce

- Autorizace uživatelů na základě rolí (+ řízení pomocí seznamů přístupu, viz výše)
- Registrace/obnova hesla pomocí emailového odkazu
- Propojení s autentizační službou (standard OAuth2/OIDC)
  - Správa uživatelů je pak řízení touto službou
- Veřejné uživatelské rozhraní pro prohlížení slovníků a pojmů
  - Lze vypnout
- REST API s dokumentací v souladu se standardem [OpenAPI](https://www.openapis.org/)
- Přehled naposled změněných a komentovaných pojmů na nástěnce aplikace
- Základní statistiky
  - Počty pojmů/slovníku/uživatelů
  - Rozložení počtů pojmů mezi slovníky
  - Rozložení klasifikace pojmů
  - Aktivita uživatelů v rámci slovníku (nové pojmy/úpravy pojmů/mazání pojmů)
- Lokalizace uživatelského rozhraní do angličtiny a češtiny
- Volitelné pravidelné emailové přehledy aktivity (změny, komentáře)
