---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: single
# title: Tutorial
permalink: /tutorial
toc: true
header:
  image: /assets/images/tutorial-header.jpg
  caption: "Photo credit: [**Immo Wegmann**](https://unsplash.com/@macroman?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText) on [**Unsplash**](http://unsplash.com/)"

---
# Basic tutorials
Tutorial on Termit basic features.
Its based on the google sheets tutorial.

This is sample of image
{% include figure image_path="/assets/images/tutorial.jpg" alt="this is a placeholder image" caption="This is a figure caption." %}

[comment]: <> Photo by <a href="https://unsplash.com/@macroman?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText">Immo Wegmann</a> on <a href="https://unsplash.com/s/photos/tutor?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText">Unsplash</a>


## TermIt Tutorial
(/A slightly modified version of the tutorial was used for user testing and evaluating its usability./)

This tutorial helps TermIt beginners understand key features of TermIt, by performing a bunch of basic tasks. 

This tutorial covers:

1) searching concepts based on their meaning and understanding the concepts, 
2) creating vocabularies,
3) creating and editing a concept in the context of related vocabularies.

TermIt serves to manage vocabularies. It supports also annotation of resources, data sets, documents and legislation. The concepts are defined inside vocabularies, where each vocabulary represents a single context. A testing version of TermIt has defined the following vocabularies (in Czech):
* vocabulary of Metropolitan plan of Prague, 
* vocabulary of Prague building regulations as of 2016, 
* vocabulary of the Act no. 183/2006 Coll.

Each vocabulary contains many terms, which are described in detail. TermIt allows organizing concepts in hieararchies, including terms coming from different vocabularies. As a result, it is possible to define that the term "Non-buildable landscape locality" from the vocabulary of the Metropolitan plan of Prague specializes the term "Locality" defined in the vocabulary of the Prague building regulations.

### Looking Up a Term
1. Go to the TermIt demo instance at https://kbss.felk.cvut.cz/termit-demo/.

2. Complete registration and log in using your username and password:
![image](https://user-images.githubusercontent.com/1140626/114211172-99bad300-9960-11eb-9222-c569a09a1238.png)

3. You are at the main dashboard of TermIt. Search the term "Estate" (in the vocabulary of the Act No. 183/2006 Coll.).
![image](https://user-images.githubusercontent.com/1140626/114211743-4e54f480-9961-11eb-99d9-1d862d5ca823.png)

4. There are two ways to get to the concept detail:
  4.1. Using the concept lookup (in the top bar).
  ![image](https://user-images.githubusercontent.com/1140626/114212951-b2c48380-9962-11eb-9f6f-4c96211bf97a.png)

  4.2. Searching the vocabulary first, and then filtering the term tree.
  ![image](https://user-images.githubusercontent.com/1140626/114213052-ce2f8e80-9962-11eb-8213-d89e1277d67f.png)
  ![image](https://user-images.githubusercontent.com/1140626/114213098-e43d4f00-9962-11eb-8820-fd9d6b9e6622.png)

5. Finally, You should have landed at the detail of the concept "Estate" in the vocabulary of the Act No. 183/2006 Coll.
![image](https://user-images.githubusercontent.com/1140626/114211949-8fe59f80-9961-11eb-8dde-83209cccbe33.png)

### Creating a Vocabulary
Now, let's create a new vocabulary. Vocabularies usually describe one particular context -- a document, data set, map, etc.

1. Click the button "New Vocabulary" in the left panel. Fill-in the vocabulary name and (optionally) also its description. In the next step we assign a file to the vocabulary.
![image](https://user-images.githubusercontent.com/1140626/114213942-f9ff4400-9963-11eb-8d9d-37c12681ccb5.png)

2. Files can be attached to a vocabulary. This includes documents which are the basis for the vocabulary, or documents which are described by the vocabulary. The document can be either an HTML file, a PDF file, an image, a map, etc. However, selection of term occurrences, definitions and performing text analysis is currently available only in HTML files. We will add add the file representing the Act No. 183/2006. You can download the file frome https://kbss.felk.cvut.cz/act-183-2006-coll.html. Then, back in TermIt, click "+ Add" next to "Files" and pick the downloaded file. In the "New file" dialog click "Create", then again "Create" in the "Create vocabulary" dialog.
![image](https://user-images.githubusercontent.com/1140626/114216344-16e94680-9967-11eb-9272-c3a1e98d4199.png)

3. The vocabulary has been created. The tab Document shows the list of attached files. Click the button "Content" to see the content of the uploaded file. In the next part we will create new terms in the vocabulary.
![image](https://user-images.githubusercontent.com/1140626/114216582-616ac300-9967-11eb-8c2b-0ee6662fba28.png)

### Creating and Editing Terms
Let's show, how to create and edit new terms and how to use them usage to annotate documents.

1. Go back to the tab "Terms". Add new terms "change in the area", "building ground" and "developed ground". According to the information in the document of the Act 183/2006. Coll. fill in their definitions and their source. Make the term "building ground" a parent of the term "developed ground". Leave other attributes empty. The steps are as follows:
2. Click "+ New term" and fill "Label" and "Text" and "Source" inside the "Definition" block. You confirm this down at the form by pressing "Create" or "Create and start new", if you want to create a new term. U pojmu "zastavěný stavební pozemek" vyberte v položce Nadřazený pojem z roletového menu "stavební pozemek". (Pozor!, nadřazený pojem už musí být vytvořen).
3. 
4. You should ![image](https://user-images.githubusercontent.com/1140626/114218131-50bb4c80-9969-11eb-82f3-64cab03e451c.png)


