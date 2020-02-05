# Detecting Cultural Violence using Natural Language processing.
This research is about detecting cultural violence by measuring the "self-other gradient" in a conflict narrative by using Natural Language Processing (NLP) technologies to understand the linguistic patterns used to legitimise violence.  The idea of cultural violence was first proposed in a 1990 paper by the Peace Researcher, Johan Galtung. In his paper he explores how aspects of culture are used to create a ‘self-other gradient’ between ‘Chosen People’ and others deemed ‘lower down the scale of worthiness’ \cite[p302]{Galtung1990}. This gradient is manifests in conflict narratives when an orator uses aspects of culture to elevate their chosen people and debase or 'otherise' their adversary. For example, with the phrase, 'God bless America’ George Bush uses religion as an aspect of culture to elevate his ingroup of America with a divine status; with the phrase ‘axis of evil’ he uses a religious concept to debase his outgroup of Iran, Iraq and North Korea. Invoking ideas of social identity theory, we refer to self as an orator’s ingroup, and the other as their outgroup \cite{Tajfel-Turner1979}. Having created a self-other gradient, violence is legitimised 'by changing the moral colour of an act from red/wrong to green/right or at least to yellow/acceptable; an example being 'murder on behalf of the country as right, on behalf of oneself as wrong’ \cite[p. 292]{Galtung1990}. Here Galtung refers to the legitimisation of military force using aspects of culture such as ideologies of national pride and international law, whereas individuals operating outside of this legitimisation framework would otherwise be committing murder. What follows is a general hypothesis in conflict narratives whereby the greater the linguistic distance between groups created by the self-other gradient, the more legitimate acts of violence against an outgroup becomes.

## Contributions
The main contributions of this paper are as follows

1. Propose cultural violence as a guiding theory for detecting harmful content in natural language.
2. Propose a novel methodology for detecting harmful content in natural language.
3. Identifying where current general purpose NLP technologies fall short in the specific task of detecting cultural violence
4. A new nlp pipeline workflow for annotating the ingroup andoutgroups in natural language texts.

## Methodology
In having proposed cultural violence as a guiding theory, we proposed the following three step methodology.

1. Detect the ingroup and outgroup of an orator's text
2. Detect how each mode of influence is used for elevating the ingroup and debase the outgroup to create a gradient between each
3. Devise a schema for measuring the gradient

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
2. A typology of cultural violence based on Mike Martin's 'Why We Fight' and Social Identity Theory for detecting aspects of culture.
3. Named Concept Recognition - Using the cultural violence typology, and seed words from each speech, a component for detecting concepts related to each aspect of culture.
