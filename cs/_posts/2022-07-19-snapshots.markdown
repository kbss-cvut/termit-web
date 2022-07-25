---
layout: single-cs
title:  "Revize"
lang: cs
categories: Dokumentace
excerpt: "Revize slouží k zakonzervování stavu slovníku v čase. "
---

[🇬🇧 English version]({{"/documentation/snapshots" | relative_url}}){: .btn .btn--info}

Revize slouží k zakonzervování stavu slovníku v čase.

Revizi vytvoříte tlačítkem Vytvořit revizi v detailu slovníku.

{% include figure image_path="/assets/images/posts/dokumentace/snapshot-1.png" alt="Revizi vytvoříte tlačítkem Vytvořit revizi v detailu slovníku." %}{: .post-image }

Revize slovníku je z pohledu ontologie zároveň slovníkem, který navíc obsahuje vazbu na původní slovník a datum vytvoření revize.

Při vytvoření revize slovníku jsou vytvořeny i revize pojmů tohoto slovníku, které jsou, stejně jako slovník, také zároveň pojmy. Kromě vazby na původní pojmy a data vytvoření všechny patří namísto do původního slovníku do jeho revize.

{% include figure image_path="/assets/images/posts/dokumentace/snapshot-2.png" alt="Schéma revizí." %}{: .post-image }

Tlačítkem vytvořit revizi vytvoříte i revize pojmů, na které mají pojmy z revidovaného slovníku a slovníků, do kterých tyto pojmy patří. Revize slovníku tedy obsahuje odkazy na pojmy z jiných slovníků ve verzi z přesného času, kdy byla revize vytvořena.

TermIt v současné době nemá nástroj pro zobrazení a procházení revizí, ale revize je možné získat pomocí služby REST API s přidáním `/versions` k URL endpointu a atributu `at` s hodnotou časové známky podle ISO 8601. Služba vrátí poslední revizi vytvořenou před zvoleným časem.

`[URL_SLUŽBY]/rest/public/terms/[NÁZEV_POJMU]/versions?namespace=[JMENNÝ_PROSTOR]&at=2022-07-04T08:50:30Z`
