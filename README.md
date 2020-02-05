# Detecting Cultural Violence using Natural Language processing.
We seek to detect cultural violence in natural language through measuring the self-other gradient. Cultural violence is a theory proposed by Johan Galtung which seeks to explain how aspects of culture - religion, ideology, language, art along with formal and empirical science - are used to legitimise violence. This notebook is focusses on the representation of religion and ideology in language. Galtung explores how each aspect can be used as a mode of influence to create a ‘self-other gradient’ between ‘Chosen People’ - referred to as an ingroup - and others deemed ‘lower down the scale of worthiness’ - referred to as an outgroup. A general thesis follows whereby the steeper the gradient, the more legitimate violence becomes. To measure the self-other gradient, therefore, means establishing a schema for measuring how aspects of culture are used to elevate the self as an ingroup and debase the other as an outgroup.

## Contributions
The main contributions of this paper are as follows

1. Propose cultural violence as a guiding theory for detecting harmful content in natural language.
  * Propose a novel methodology for detecting harmful content in natural language.
  * Identifying where current general purpose NLP technologies fall short in the specific task of detecting cultural violence
  * A new nlp pipeline workflow for annotating the ingroup andoutgroups in natural language texts.

## Methodology
In having proposed cultural violence as a guiding theory, we proposed the following three step methodology.

1. Detect the ingroup and outgroup of an orator's text
.. Detect how each mode of influence is used for elevating the ingroup and debase the outgroup to create a gradient between each
.. Devise a schema for measuring the gradient

For the detectiong of cultural violence in natural langugage we test existing Natural Language Processing (NLP) technologies for each .. step of the methodology from which new pipeline components have been devised. NLP is a branch of artificial intelligence which seeks to process natural language to derive meaning. In general terms there are two fields of NLP, theoretical and applied. Theoretical NLP is concerned with the technical aspects of processing language and Applied NLP is concerned with the application of such technologies. The technologies we test are from the spaCy library for Python. This research sits within applied NLP and in seeking to qualify sociological theory sits within the field of the Digital Humanities.

## Dataset
The datasets we are using for these test are speech transcripts of George Bush and Osama bin Laden from the War on Terror in which they advocated violence, therefore, these datasets contain cultural violence. As a reference dataset we use speeches made by Martin Luther King who uses many of the same aspects of culture used by Bush and bin Laden, but he does not advocate for violence. The difference between Luther King's and the other speeches, therefore, may reveal the defining features of culturally violent language.

## Tests
The tests are as follows:

A test of named entity recognition in the spaCy language models against the dataset.
A test of sentiment analysis technologies for detecting the ingroup and outgroup of a text.
Detailed testing of the Watson API
From these tests, the following spaCy pipeline components have been created:

1. Supplemtary Named Entity Recognition - contains corrections for named entities either not identified or incorrectly identified by the model.
.. A typology of cultural violence based on Mike Martin's 'Why We Fight' and Social Identity Theory for detecting aspects of culture.
.. Named Concept Recognition - Using the cultural violence typology, and seed words from each speech, a component for detecting concepts related to each aspect of culture.
