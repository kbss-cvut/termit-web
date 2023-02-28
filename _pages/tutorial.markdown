---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: single
title: Tutorial
permalink: /tutorial
lang: en
lang-ref: tutorial
author_profile: true
header:
  image: /assets/images/tutorial-header.jpg
  caption: "Photo credit: [**Immo Wegmann**](https://unsplash.com/@macroman?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText) on [**Unsplash**](http://unsplash.com/)"
toc: true
---

<!-- # Tutorial -->

TermIt is designed for terms and vocabularies management. It allows users to assign terms from the specific vocabularies to the documents or any other resources and interconnect them. The basic tutorial describes following activities:
* searching terms and browsing vocabularies,
* marking occurrences of terms and their definitions in documents,
* creating and editing vocabularies and terms,
* assigning document to the vocabulary and its annotation.

Advanced tutorial and documentation describing all tools in TermIt is under construction.

## Sandbox
The page <a href="https://kbss.felk.cvut.cz/termit-demo">https://kbss.felk.cvut.cz/termit-demo</a> contains a live demo version of TermIt. It allows various levels of access based on the user role:

* Guest -- it is possible only to browse data, it is not possible to edit term or vocabularies, show documents or other sources. Functionality is very limited. This regime serves to the public to view the data.
* Reader -- readers may browse vocabularies, terms and sources. They can see additional details of terms and vocabularies, show definition of a term in a document and comment. They cannot edit or create new terms or vocabularies. This regime serves for users from within the organization that want to comment the work.
* Editor -- users have full rights to browse, edit and create terms, vocabularies and sources and can also annotate documents. This regime is intended for domain experts. They are usually the main creators of the vocabularies. This role must be granted by an administrator. If you register to the live demo, this is the role you will get.
* Administrator -- administrator has full access to all features, including assigning roles of other users and creating new users.

We recommend installing a local instance of TermIt (use guide in <a href="/install">tab Install</a>).

## Basic tutorial

Basic tasks -- those comprising most of the work usually done in TermIt -- are briefly described in the basic tutorial.

### Searching terms and browsing vocabularies

Searching terms is an elementary task. Term in TermIt is a concept in specified context, e.g. 'construction' may be represented by two terms, where one stands for a constructed object (building) and second one represents a process of a constructing a building. Terms are usually defined in a context of a vocabulary, e.g. vocabulary of a specific legislative document (construction in a meaning of a specific law) or a specific data set (set of ongoing constructions of building within a municipality).

Let's find a term "Building" from the vocabulary 'Vocabulary of Prague Building Regulations 2016'.

#### Search bar
The easiest way of searching terms is typing their name (label) into the search bar in the upper part of the page.

{% include figure image_path="/assets/images/tutorial/search-bar.png" alt="Searching for a term using search bar" caption="Searching for a term using search bar." %}

By pressing enter you get search details. Results contain label, type (term, vocabulary, document...) and source. Clicking a term shows its details.

#### Browsing vocabularies

Another way is browsing vocabularies. Click on "vocabularies" in the left panel to see the list of vocabularies. Above the list is a text field for filtering. Use it to filter out the vocabulary called 'Vocabulary of Prague Building Regulations 2016'.

{% include figure image_path="/assets/images/tutorial/vocabularies.png" alt="Filtering vocabulary" caption="Filtering vocabulary." %}

Clicking the vocabulary shows its detail. Below the basic details is open tab 'Terms' with the list of all terms in a hierarchic structure. Empty text box above allows filtering terms.

{% include figure image_path="/assets/images/tutorial/terms-in-vocab.png" alt="Browsing terms in a vocabulary" caption="Browsing terms in a vocabulary." %}

Click the term to show its detail.

#### Term detail

Term detail contains basic information about the term, hierarchic structure of other terms in the same vocabulary and detailed information about the term in tabs in the lower part of the page.

{% include figure image_path="/assets/images/tutorial/detail-1.png" alt="Term details" caption="Term details." %}

### Marking occurrences of terms and their definitions in documents

Vocabularies are usually interconnected to the documents containing their definitions and occurrences. Open  'Vocabularies' in the left panel and search for the vocabulary 'Vocabulary of Building Act no. 72/2004 of the New Zealand'. In the vocabulary detail open tab 'Document'.

{% include figure image_path="/assets/images/tutorial/vocab-detail.png" alt="Detail of a document assigned to the vocabulary" caption="Detail of a document assigned to the vocabulary." %}

Document information contain document label, its description and list of assigned terms. Those terms have marked occurrences in the document. Below is a list of files belonging to the document. Building Act has only one called 'building-act.html'. By clicking 'Show Content' next to the label you get to the file content.

{% include figure image_path="/assets/images/tutorial/document-content.png" alt="Content of a document with marked term occurrences and definition" caption="Content of a document with marked term occurrences and definition." %}

Green colored terms are occurrences of terms, blue colored are definitions of terms. Click on them to show pop-up with information which term is marked. You can remove or edit the occurrence in the pop-up. Clicking the label redirects you to the term detail.

{% include figure image_path="/assets/images/tutorial/occurrence.png" alt="Occurrence detail" caption="Occurrence detail." %}

[comment]: <> přidat označování výskytů a definic

### Creating new vocabularies and terms

In this task we will create new vocabulary, assign a document to it and create few terms. Make sure you have at least the 'Editor' user role.

### Creating new vocabulary

Click 'New Vocabulary' in the left panel. In the Create vocabulary form fill label and description.

{% include figure image_path="/assets/images/tutorial/new-vocab.png" alt="Create new vocabulary form" caption="Create new vocabulary form." %}

During the creation of a vocabulary, a document with a file can be created and assigned to it. If you want to mark occurrences in the file later, upload file in HTML (other formats may be uploaded, but cannot yet be marked or analyzed). Download any legislation document from EUR-Lex in the HTML format, e.g. <a href="https://eur-lex.europa.eu/legal-content/EN/TXT/HTML/?uri=CELEX:22016A1019(01)&from=EN">Paris Agreement</a>. In the create vocabulary dialogue, click '+ Add' next to the Files below Description and select the downloaded HTML file. Fill matching label and click 'Upload' and then 'Create'to create vocabulary.

In the upper right corner of the page appear several green popups confirming the successful creation of the new vocabulary. They disappear after a while.

{% include figure image_path="/assets/images/tutorial/vocabulary.png" alt="New vocabulary is successfully created" caption="New vocabulary is successfully created." %}

#### Creating new terms

Terms may be created in the vocabulary detail or directly in the file of a document. This part of tutorial focuses on the creation of terms from the vocabulary.

Go into the Terms tab in the detail of your vocabulary (it shall be open as you open the vocabulary detail). Click the '+ New term' button.

Fill the following attributes in the new term dialogue:

* label: 'Climate change' -- title of a term, serves for recognition and unique identification within the vocabulary,
* synonyms: 'Climate emergency' -- alternate titles or names. Serves mostly for annotation and search. Synonym must be confirmed by clicking '+ Add',
* definition, text: 'A change of climate which is attributed directly or indirectly to human activity that alters the composition of the global atmosphere and which is in addition to natural climate variability observed over comparable time periods.' -- unique definition of a term in a given context, usually marked in the document. Every term has exactly one definition,
* definition, source: 'https://unfccc.int/resource/docs/convkp/conveng.pdf, Article 1, 2.' -- mark a source of definition as a text or link to the external source.

Leave other fields blank and click 'Create and Start New'.

{% include figure image_path="/assets/images/tutorial/climate-change.png" alt="Creation of a new term" caption="Creation of a new term." %}

In the similar way create terms 'Climate system', 'Emissions' and 'Greenhouse gases'. They are defined in the UNFCCC document, too.

Upper part of dialogue allows users to add tab with different language. Every deployment has one default (and required) language. For live demo deployment it is English.

#### Term control and editing

When you go back to the vocabulary, tab 'Terms' is filled with the terms we have just created. Every term has a colored dot before the label. Its color stands for the term completeness.

{% include figure image_path="/assets/images/tutorial/validation.png" alt="List of new terms with validation markers." caption="List of new terms with validation markers." %}

Open one of the terms and check the tab 'Validation'.

{% include figure image_path="/assets/images/tutorial/control.png" alt="Results of the term completeness control" caption="Results of the term completeness control." %}

The picture above shows the validation results. No results mean a complete term. We will fix the term by the term editing. Click 'Edit' in the upper right corner of the term detail. Shown dialogue is same as for the term creation, but attribute values are already filled.

**The concept does not have defined nor inferred content type**

Content types define the character of a term and is important to interconnect terms within the semantic models and inference of new knowledge. We distinguish types ('car manufacturer') and individuals ('Ford') in four basic categories:

* object/object type, -- independent elements changing over time,
* intrinsic trope/intrinsic trope type -- qualitative or quantitative trope dependent on object,
* relator/relator type -- interconnection of two (or more) objects dependent on them,
* event/event type -- independent element temporally immutable (completely finished in past).

Value of the attribute 'Type' of term 'Emissions' set to 'Object type'.

**The term does not have a source**

Definition of a term consists of a text and a source. Both elements are required for 100% completeness of a term. Fill a text (e.g. Article 1, 2. of UNFCCC) to the source field to get rid of this result.

**The term does not have a parent**

Terms in TermIt have hierarchical structure. Attribute 'Parent terms' may link to the term from the same or imported (described further in tutorial) vocabulary.

Check the validation tab again. Some results shall disappear. The corrected terms have now green dot next to it.

By editing, you may fix other terms completeness as well.

[comment]: <> přidej sekci #### Závislost pojmů

### Annotate documents

This part of tutorial works with the document uploaded during the vocabulary creation. In the vocabulary details open tab 'Document' and 'Show Content' of Paris Agreement.

{% include figure image_path="/assets/images/tutorial/show-file.png" alt="Show a file belonging to the document assigned to the vocabulary" caption="Show a file belonging to the document assigned to the vocabulary." %}

Vocabulary already contains some terms (those created directly in the vocabulary). Run the text analysis of a file using our vocabulary. In the upper bar click 'Analyze'. In the pop-up select your vocabulary and click 'Analyze' in the pop-up.

{% include figure image_path="/assets/images/tutorial/analyze.png" alt="Dialogue for selection of a vocabulary used for analysis" caption="Dialogue for selection of a vocabulary used for analysis." %}

Analyze may take some time (based on the file size). Analysis results are suggested occurrences of existing terms and suggestions of new terms based on the frequency of their occurrence in the document.

{% include figure image_path="/assets/images/tutorial/analysis-output.png" alt="File analysis results" caption="File analysis results." %}

#### Term occurrence confirmation

Terms marked green with dotted border are suggested occurrences of existing terms. Click on one of them to see pop-up with a suggestion. 'Tick' for the confirmation of the occurrence of suggested term or click a pencil symbol to select other existing term. Trash can symbol removes the occurrence and cross closes pop-up.

{% include figure image_path="/assets/images/tutorial/confirm-occurrence.png" alt="Confirmation of suggested occurrence of an existing term" caption="Confirmation of suggested occurrence of an existing term." %}

#### Creating new term based on a suggestion

Terms marked red with a dotted border are suggested occurrences of terms that do not yet exist. Open a pop-up by clicking the term. You may select an existing term or click '+ Add' to create a new one.

{% include figure image_path="/assets/images/tutorial/create-suggested-term.png" alt="Creation of a new term based on a suggested occurrence" caption="Creation of a new term based on a suggested occurrence." %}

New pop-up appears. Dialogue is very similar to the creation of a new term directly from vocabulary with one exception. Definition of a term may be selected directly from the text of a document. Click 'Select definition', then mark a definition text from the file. It appears in the form. You may edit it.

{% include figure image_path="/assets/images/tutorial/select-definition.png" alt="Dialogue to create a new term from the text of a document file" caption="Dialogue to create a new term from the text of a document file." %}

After creating a term its occurrence is marked green and its definition blue.

{% include figure image_path="/assets/images/tutorial/occurrence-definition.png" alt="Marking of term occurrence and definition" caption="Marking of term occurrence and definition." %}

#### Creating new term from text

Term may be created even if it was not suggested automatically by the annotator. Select a text with the term you want to create to show a pop-up. You may choose between 'Mark term occurrence', where you can either select existing term or create a new one in the same way as in the previous section, opr you my mark a definition of a term.

{% include figure image_path="/assets/images/tutorial/select-text.png" alt="Selection of a text for creation of an occurrence or definition" caption="Selection of a text for creation of a an occurrence or definition." %}

#### Mark term definition

From the text selection pop-up choose 'Mark term definition'. Select a term whose definition was selected. Then you see a pop-up with the selected text and source, where you may edit the text and add source. If you select a term that already has a definition, you can see both new and old definition text and source, but you may edit only the new one, which remains after saving.

{% include figure image_path="/assets/images/tutorial/definition.png" alt="Edit definition text and source" caption="Edit definition text and source." %}
