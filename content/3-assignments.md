---
title: (Voluntary) Assignments
nav: Assignments
---

# Assignment 1 (Network Analysis)

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

## Example solution

* [Minimal and barely commented solution notebook](https://sds-aau.github.io/SDS-master/M2/exercises/nw_assignment_solution.nb.html): Shows you some fast and easy ways how to solve the assignment tasks. Doesn't explain a lot, but will help to get you started and/or check if you are on the right track. Please give it a shot on your own before, though :)
* [Minimal solution Py](https://colab.research.google.com/github/SDS-AAU/SDS-master/blob/master/M2/exercises/M2_workshop_NW_Assignment_solution.ipynb){:target="_blank"} 


# Assignment 2 - NLP and Presidential Debate Tweets

Using the below data of tweets about the presidential debate in the US (autumn 2020) as well as the tweets of US Congress members by Party, we would like you to classify the debate-tweets into conservative vs. liberal. Using techniques learned in the course provide some insights about what most conservative the and most liberal posts are talking about...

- The data is gz-compressed JSON format - in Python pandas should not have issues opening it with `pd.read_json`, otherwise add `compression='gzip'` 

- in R:

```{% raw %}
library(jsonlite)
tmp <- tempfile()
download.file("https://github.com/SDS-AAU/SDS-master/raw/master/M2/data/pol_tweets.gz", tmp)

tweets_raw <- stream_in(gzfile(tmp, "pol_tweets")){% endraw %}
```

* 50k tweets from members/groups in the US Congress by Party (Rep:0, Dem:1: `https://github.com/SDS-AAU/SDS-master/raw/master/M2/data/pol_tweets.gz`
* ~8k tweets on the 2020 presidential debate: `https://github.com/SDS-AAU/SDS-master/raw/master/M2/data/pres_debate_2020.gz`

## Example solution

* [Solution Py](https://colab.research.google.com/github/SDS-AAU/SDS-master/blob/master/M2/exercises/Poltweets_assignment_solution.ipynb){:target="_blank"} 
* [(Minimal) Solution R](https://sds-aau.github.io/SDS-master/M2/exercises/NLP_workshop_1_debate_tweets.nb.html#Simple_test)
* [Solution add-on transformers](https://colab.research.google.com/github/SDS-AAU/SDS-master/blob/master/M2/exercises/transformer_pol_tweets_solution.ipynb){:target="_blank"} 
* [Video walktrough](https://www.loom.com/share/83dc5e5a1bbe48d6a241ebe6e2b52c4c){:target="_blank"} 
