---
title: Network Analysis
nav: Network Analysis
---

Contents & Topics: 

* Network thinking
* Types of Networks & Sources of Network Data
* Network Visualization
* Network-based indicators
* Community Detection
* Networks and Supervised Machine Learning


# Theory: Introduction to network analysis

* Introduction to network analysis: 
   * [Video](https://www.loom.com/share/307f388fbb3d4e73919250aa6eb535f0) 
   * [Slides](https://sds-aau.github.io/SDS-master/M2/notebooks/network_analysis_theory.html)

# Applied Network Analysis (R & Python)

## Applied Introduction

* R: 
   * Video [1: Intro & ecosystem](https://www.loom.com/share/abe75a61d7374ae99f946e1a5829430e) [2: Network Measures](https://www.loom.com/share/981c493c990c46f591f465455a0d5bba) [3: Mini Case](https://www.loom.com/share/9fc0c009945c4fb0b3aaa0be77f52707) 
   * [Html](https://sds-aau.github.io/SDS-master/M2/notebooks/network_analysis_application.nb.html) 
   * [Colab](https://colab.research.google.com/github/SDS-AAU/SDS-master/blob/master/M2/notebooks/network_analysis_application.ipynb)
   * Exercises: [1: Basics](https://colab.research.google.com/github/SDS-AAU/SDS-master/blob/master/M2/exercises/network_analysis_application_ex1.ipynb)

* Python: 
   * Video [1: Intro & ecosystem](https://www.loom.com/share/e2a1e501c1474b70aaa64bad5257d635)  [2: Network Measures](https://www.loom.com/share/3556014c3e2b4fd39d675e05258f5041) [3: Mini Case](https://www.loom.com/share/75ed0b7f781a447991f28149bbe54c04) 
   * [Colab](https://github.com/SDS-AAU/SDS-master/blob/master/M2/notebooks/M2_Networks_hands_on_in_python.ipynb)

## Intermediate Network Analysis Directed & Social networks

* R: 
   * [Video](https://www.loom.com/share/1f905b64ba014819a0c0b45c0757f92c) 
   * [Html](https://sds-aau.github.io/SDS-master/M2/notebooks/network_analysis_application_directed.nb.html) 
   * [Colab](https://colab.research.google.com/github/SDS-AAU/SDS-master/blob/master/M2/notebooks/network_analysis_application_directed.ipynb)

* Python: 
   * Video [1: DiGraphs-intro](https://www.loom.com/share/6a8c8d5d6b8e4e989356b5ca4fa47035?sharedAppSource=personal_library)  [2: DiGraphs-Case](https://www.loom.com/share/fb7a9e91d67e487094b390c9b509737c?sharedAppSource=personal_library) 
   * [Colab](https://github.com/SDS-AAU/SDS-master/blob/master/M2/notebooks/M2_Directed_Networks_hands_on_Python.ipynb)

## Bipartite (2-mode) Networks

* R: 
   * Video [1: Bipartite NW structures](https://www.loom.com/share/7668a71c95f941a1a17148e45ba83689) [2: Application Bibliometric Networks](https://www.loom.com/share/2fdf16a87a9d4eac81d50cef0b55ae3b) 
   * [Html](https://sds-aau.github.io/SDS-master/M2/notebooks/network_analysis_application_bipartite.nb.html) 
   * [Colab](https://colab.research.google.com/github/SDS-AAU/SDS-master/blob/master/M2/notebooks/network_analysis_application_bipartite.ipynb)

* Python: 
   * Similarity and Bipartite NWs [Video](https://www.loom.com/share/f51efae898ff4d78a69949381b4649fe) 
   * [Colab](https://nbviewer.jupyter.org/github/SDS-AAU/SDS-master/blob/master/M2/notebooks/M2_Bipartite_graphs_in_Python.ipynb)
   * Mapping ETF Holdings with NWs [Video](https://www.loom.com/share/3984d91363f54c01b27d8672f382b711?sharedAppSource=personal_library) 
   * [Colab](https://nbviewer.jupyter.org/github/SDS-AAU/SDS-master/blob/master/M2/notebooks/M2_Case_ETF_Holdings_Python.ipynb)


# General Data Science Resoures

## R
* Wickham, H., & Grolemund, G. (2016). R for data science: import, tidy, transform, visualize, and model data. O'Reilly Media, Inc. [Online available here](https://r4ds.had.co.nz/)
* Baumer, B., Kaplan, D. & Horton, N. (2020) Modern Data Science with R (2nd Ed.). CRC Press [Online available here](https://beanumber.github.io/mdsr2e/)
* Kuhn, M., Silge, J. (2020) Tidy Modeling with R [Online available here](https://www.tmwr.org/)


## Python

* VanderPlas, J. (2016). Python data science handbook: Essential tools for working with data. O'Reilly Media, Inc. [Online available here](https://jakevdp.github.io/PythonDataScienceHandbook/index.html)


# Assignment 1

## Introduction

* In th first Part 2, you will replicate a well known network analysis, with different data and some twists. 
* Data: The data is to be found at: https://github.com/SDS-AAU/SDS-master/raw/master/00_data/network_krackhard 

## Data: What do I get?

### Background
Let the fun begin. You will analyze network datacollected from the managers of a high-tec company. This dataset, originating from the paper below, is widely used in research on organizational networks. Time to give it a shot as well.
Krackhardt D. (1987). Cognitive social structures. Social Networks, 9, 104-134. The company manufactured high-tech equipment on the west coast of the United States and had just over 100 employees with 21 managers. Each manager was asked to whom do you go to for advice and who is your friend, to whom do you report was taken from company documents.
Description

The dataset includes 4 files - 3xKrack-High-Tec and 1x High-Tec-Attributes. Krack-High-Tec includes the following three 21x3 text matrices:

* ADVICE, directed, binary
* FRIENDSHIP, directed, binary
* REPORTS_TO, directed, binary

Column 1 contains the ID of the ego (from where the edge starts), and column 2 the alter (to which the edge goes). Column 3 indicates the presence (=1) or absence (=0) of an edge.

High-Tec-Attributes includes one 21x4 valued matrix.

* ID: Numeric ID of the manager
* AGE: The managers age (in years)
* TENURE: The length of service or tenure (in years)
* LEVEL: The level in the corporate hierarchy (coded 1,2 and 3; 1 = CEO, 2 = Vice President, 3 = manager)
* DEPT: The department (coded 1,2,3,4 with the CEO in department 0, ie not in a department)


## Tasks

### 1. Create a network

* Generate network objects for the companies organizational structure (reports to), friendship, advice
* This networks are generated from the corresponding edgelists
* Also attach node characteristics from the corresponding nodelist

### 2. Analysis

Make a little analysis on:

A: Network level characteristics. Find the overal network level of:

* Density
* Transistivity (Clustering Coefficient)
* Reciprocity

... for the different networks. Describe and interpret the results. Answer the following questions:

* Are relationships like friendship and advice giving usually reciprocal?
* Are friends of your friends also your friends?
* Are the employees generally more likely to be in a friendship or advice-seeking relationship?

B: Node level characteristics: Likewise, find out:

* Who is most popular in the networks. Who is the most wanted friend, and advice giver?
* Are managers in higher hirarchy more popular as friend, and advice giver?

C: Relational Characteristics: Answer the following questions:

* Are managers from the same 1. department, or on the same 2. hirarchy, 3. age, or 4. tenuere more likely to become friends or give advice? (hint: assortiativity related)
* Are friends more likely to give each others advice?


### 3. Visualization

Everything goes. Show us some pretty and informative plots. Choose what to plot, and how, on your own. Interpret the results and share some insights.



