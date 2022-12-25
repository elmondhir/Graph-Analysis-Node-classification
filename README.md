CrowdSec is an open-source and lightweight software that allows you to detect peers with malevolent behaviors and block them from accessing your systems at various levels (infrastructural, system, applicative).

Take a look at the [official documentation](https://doc.crowdsec.net/docs/intro) of the CrowdSec software to understand context of the collected data. 
# Introduction

The goal of this homework assignment is to assess the ability to deal with real data used in cybersecurity, approaches to the problem, and basic concepts in data science (EDA, visualization, model training, ... ).

## **Summary** : 

- **EDA** :  
    - Data cleaning 
    - Data preprocessing
    - Feature Engineering
    - Answering key questions about the data
        * What is the distribution of the attack type in terms of the number of IPs reported? 
        * What are the names of the top 10 AS hosting the highest number of malicious IPs? 
        * What are the names of the top 10 AS hosting malicious IPs which perform the highest number of attack? 
        * What are the 10 watchers IDs which suffered from the highest number of attacks ?
        * Compare the distribution of the average `activity_in_days` and `age_in_days` of the watchers who reported each malicious IPs. 
        
- **Graph** : Build a  graph $G = (V,E)$ where a node $v$ is a malicious IP and an edge $e$ links two malicious IPs if they were reported by the same watcher. Hence the edges are weighted by the number of times 2 malicious IPs were reported by the same watchers.
    * Visualization: 
        * Plot a heatmap of the adjacency matrix of the top 40 most connected nodes
        * Plot the subgraph of the 40 most connected nodes



- **Attack type classifier** :
    - Implementation of GCN (graph convolutional network) for node classification (Attack type)

- **Classification with semi supervised learning** : (is_malicious IP_validated)
    - Label propagation

- **Hyperparameter tuning** : 
    - Using Optuna framework


### Author : **CHAALAL Mohamed Elmondhir*.
