---
title: Home
layout: default
---

# Working with unstructured data

{% include figure.html img="titlepage.jpg" alt="intro image here" caption="Unsplash, Franki Chamaki" width="75%" %}

This is the repository website for the 2021 course in Network Analysis and NLP at the UNISTRA DS programme. On this page you will find tutorial videos, assignments and links to Q&A meetings. The page is updated throughout the course.


{% capture text %}
- Network thinking
- Types of Networks & Sources of Network Data
- Network Visualization
- Network-based indicators
- Community Detection
- Networks and SML

### Ecosystem
**R**
- [Tidyverse](https://www.tidyverse.org/): General datascience ecosystem for R
- [Igraph](https://igraph.org/): Main graph analytics package in R
- [Tidygraph](https://tidygraph.data-imaginist.com/): Igraph wrapper for tidy network analytics workflows
- [Ggrph](https://ggraph.data-imaginist.com/): ggplot2 extension for network visualization

**Python**
- [NetworkX](https://networkx.org/) - standard library for NA in Python
- [pyvis](https://pyvis.readthedocs.io/en/latest/) - useful visualisation package


{% endcapture %}
{% include card.html text=text header="Part 1: Network Analysis" title="Contents" img="network_title.jpg" %}


{% capture text %}
- Simple frequency based approaches
- Co-occurrence and link to networks
- Topic Modelling
- Vectorisation and embeddings
- NLP and SML

### Ecosystem
**R**
- [tidytext](https://juliasilge.github.io/tidytext/) - Main NLP and textmining ecosystem for R.
- [Quanteda](https://quanteda.io/) - Further NLP functionalities in this popular package in R.

**Python**
* [NLTK](https://www.nltk.org/book/) - Standard library for all traditional NLP work in Python
* [SpaCy](https://spacy.io/) - modern deep learning based library for many NLP tasks
* [Gensim](https://radimrehurek.com/gensim/) - library for topic modelling and vectorisation
* [Textblob](https://textblob.readthedocs.io/en/dev/) - simple library wrapping NLTK ... but simpler

{% endcapture %}
{% include card.html text=text header="Part 2: Natural Language Processing" title="Contents" img="nlp_title.jpg" %}


------

{% include template/credits.html %}
