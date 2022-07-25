---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: single-cs
title: Technické detaily
permalink: /cs/technical-details
lang: cs
lang-ref: technical-details
header:
  image: /assets/images/data-model-header.jpg
  caption: "Photo credit: [**Toby56**](https://unsplash.com/@toby56?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText) on [**Unsplash**](http://unsplash.com/)"
toc: true
---

<!-- # Technické detaily -->

Tato stránka obsahuje další technické pozadí systému TermIt. Popisuje architekturu systému, knihovny, které jsme vyvinuli a které TermIt používá a datový model použitý v základní verzi TermItu.

## Technologie a architektura

Technicky je TermIt webová aplikace. Systém je rozdělen do dvou sub-projektů: jeden reprezentuje serverovou část, druhý klientskou část. Architektura systému je ukázána v následujícím diagramu.

{% include figure image_path="/assets/images/technical-details/termit-architecture.png" alt="TermIt architecture diagram" caption="Diagram architektury systému TermIt" %}

### Serverová část systému TermIt

Serverová část systému je napsána v jazyce Java (8 nebo novější). Jedná se o Java aplikaci založenou na [Spring Boot](https://spring.io/projects/spring-boot) s REST API podporujícícm JSON a [JSON-LD](https://json-ld.org/). TermIt běží nad triple storem, kam ukládá všechna data. Systém byl testován nad [RDF4J](https://rdf4j.org/) a [GraphDB](https://graphdb.ontotext.com/), která poskytuje stabilnější výkon.

Detailní popis konfigurace a vývoje serverové části TermItu je k nahlédnutí v [tomto GitHub repositáři](https://github.com/kbss-cvut/termit).

### Klientská část systému TermIt

Klientská část systému je napsaná v TypeScriptu, používající [React framework](https://reactjs.org/). Ten je použit pro svou jednoduchost a rozsáhlý ekosystém knihoven.

Zdrojový kód klientské části je v [tomto GitHub repositáři](https://github.com/kbss-cvut/termit-ui), který obsahuje i základní vývojářskou dokumentaci.

### Integrace s nástrojem Annotace

Jednou z nejdůležitějších funkcí systému TermIt je jeho schopnost analyzovat obsah dokumentů pro vyhledávání výskytu existujících pojmů a navrhování nových pojmů podle jejich významu v textu. Textovou analýzu zajišťuje samostatně vyvinutá open-source knihovna **Annotace**, kterou můžete najít v [jejím GitHub repozitáři](https://github.com/kbss-cvut/annotace).


### Zajímavé knihovny

TermIt používá několik knihoven vyvinutých pro účely sémantického webu a sémantických dat, a které by mohly zajímat i další vývojáře v této obasti. Jsou shrnuty v následujícím seznamu včetně základního popisu a odkazu.

#### JOPA

[JOPA](https://github.com/kbss-cvut/jopa) (Java OWL Persistence API) je perzistentní knihovna pro sémantická data. Umožuje práci s doménovým modelem založeným na POJO, který je uložen v podobě RDF dat v triple storu. Silná inspirace v JPA je vidět i v přítomnosti transakcí, mapování výsledků dotazů a cachování za účelem co nejhladšího vývoje informačního systému založeného na principech sémantického webu.

Pro integraci JOPA s deklarativní správou transakcí Springu (`@Transactional`), která je použita v systému TermIt je zde i [tato knihovna](https://github.com/ledsoft/jopa-spring-transaction).

#### JB4JSON-LD
[JB4JSON-LD](https://github.com/kbss-cvut/jb4jsonld) (Java Binding for JSON-LD) je knihovna pro snadné mapování POJO na JSON-LD a naopak. Integruje se s Jacksonem, takže použití v aplikaci je otázkou pouze několika řádek kódu.

## Datový model

Slovníky modelované v systému TermIt používají pro data dva datové modely -- ontologii Popis dat a TermIt ontologii. Oba modely byly vytvořeny skupinou Knowledge-based and Software Systems Group (KBSS).

### Ontologie popis dat

Základní ontologie použitá k popisu (libolovných) dat se jmenuje Popis dat a její dokumentaci [najdete na této stránce](http://onto.fel.cvut.cz/ontologies/slovnik/agendovy/popis-dat/current/index-cs.html). Ontologie je založena na Unified Foundational Ontology (UFO) a je určena k popisu libovolných datových zdrojů, např. databází, dat v různých souborových formátech, souborů atd.

Současnou verzi ontologie Popis dat můžete najít [zde](https://onto.fel.cvut.cz/ontologies/page/slovnik/agendovy/popis-dat/model/verze/1.0.1) ve formátu turtle nebo v RDF/XML.

Následující sekce popisují základní třídy definované v datovém modelu.

#### Slovník
Slovník reprezentuje ontologii, která se skládá z glosáře a modelu.

#### Glosář
Glosář je seznam všech pojmů ve slovníku a používá koncepty ze slovníku SKOS.

#### Model
Model propojuje pojmy definované v glosáři za pomoci ontologických vztahů, především pocházejících z ontologie UFO.

#### Term
Term je libovolný pojem ve slovníku.

#### Zdroj
Zdroj představuje původ dat, která jsou modelována, například databáze, soubor atd.

#### Atribut
Atribut je speciální případem termu, který představuje vlastnost závislou na předmětu popsaném ve zdroji (např. sloupec v databázové tabulce, vlastnost popsaná v dokumentu atd.).

### Ontologie TermIt

Ontologie TermIt je vytvářena během vývoje systému TermIt. Dědí od obecné ontologie Popis dat a rozšiřuje jí o koncepty používané specificky v systému TermIt.

Ontologie TermIt obsahuje například pojmy popisující anotaci textů, výskyty pojmů ve zdrojích a správu uživatelů.

Aktuální verze ontologie TermIt je součástí základní verze termitu a je dostupná z [repozitáře TermItu na GitHubu](https://github.com/kbss-cvut/termit/tree/master/ontology).
