# Detecting Cultural Violence using NLP.
---
This research is about detecting cultural violence by measuring the "self-other gradient" in a conflict narrative by using Natural Language Processing (NLP) technologies to understand the linguistic patterns used to legitimise violence.  The idea of cultural violence was first proposed in a 1990 paper by the Peace Researcher, Johan Galtung. In his paper he explores how aspects of culture are used to create a ‘self-other gradient’ between ‘Chosen People’ and others deemed ‘lower down the scale of worthiness’ . This gradient is manifests in conflict narratives when an orator uses aspects of culture to elevate their chosen people and debase or 'otherise' their adversary. For example, with the phrase, 'God bless America’ George Bush uses religion as an aspect of culture to elevate his ingroup of America with a divine status; with the phrase ‘axis of evil’ he uses a religious concept to debase his outgroup of Iran, Iraq and North Korea. Having created a self-other gradient, violence is legitimised 'by changing the moral colour of an act from red/wrong to green/right or at least to yellow/acceptable; an example being 'murder on behalf of the country as right, on behalf of oneself as wrong’. Here Galtung refers to the legitimisation of military force using aspects of culture such as ideologies of national pride and international law, whereas individuals operating outside of this legitimisation framework would otherwise be committing murder. What follows is a general hypothesis in conflict narratives whereby the greater the linguistic distance between groups created by the self-other gradient, the more legitimate acts of violence against an outgroup becomes.

## Tests
IN the repository we present a number of experiments used to assess necessary modification to :

1. A test of named entity recognition in the spaCy language models against the dataset.
2. A test of sentiment analysis technologies for detecting the ingroup and outgroup of a text.
3. Detailed testing of the Watson API

From these tests, the following spaCy pipeline components have been created:

1. Supplemtary Named Entity Recognition - contains corrections for named entities either not identified or incorrectly identified by the model.
2. Named Concept Recognition - Using the novel typology of groups, and seed words from the dataset, a component for detecting concepts related to each aspect of culture.

## Contributions
The main contributions of this research are as follows

1. Propose a novel methodology for detecting harmful content in natural language.
2. Propose cultural violence as a guiding idea for detecting harmful content in natural language.  
3. Present a typology of social groups
4. A new nlp pipeline workflow for annotating the ingroup and outgroups in natural language texts.
5. Identify imporovements to general purpose NLP technolgies for the specific task of detecting cultural violence.

## Methodology
In having proposed cultural violence as a guiding theory, we proposed the following three step methodology.

1. Detect the ingroup and outgroup of an orator's text
2. Detect and classify phrases with an intent to elevate an ingroup.
3. Detect and classify phrases with an intent to debase an outgroup.
4. Apply a measurement schema to these phrases to determine gradient between ingroup and outgroup.

For the detectiong of cultural violence in natural langugage we test existing Natural Language Processing (NLP) technologies for each step of the methodology from which new pipeline components have been devised. NLP is a branch of artificial intelligence which seeks to process natural language to derive meaning. In general terms there are two fields of NLP, theoretical and applied. Theoretical NLP is concerned with the technical aspects of processing language and Applied NLP is concerned with the application of such technologies. The technologies we test are from the spaCy library for Python. This research sits within applied NLP and in seeking to qualify sociological theory sits within the field of the Digital Humanities.

## Dataset
The datasets we are using for these test are speech transcripts of George Bush and Osama bin Laden from the War on Terror in which they advocated violence, therefore, these datasets contain cultural violence. As a reference dataset we use speeches made by Martin Luther King who uses many of the same aspects of culture used by Bush and bin Laden, but he does not advocate for violence. The difference between Luther King's and the other speeches, therefore, may reveal the defining features of culturally violent language.


