CrowdSec is an open-source and lightweight software that allows you to detect peers with malevolent behaviors and block them from accessing your systems at various levels (infrastructural, system, applicative).

Take a look at the [official documentation](https://doc.crowdsec.net/docs/intro) of the CrowdSec software to understand context of the collected data. 
# Introduction

The goal of this homework assignment is to assess my ability to deal with real data used in cybersecurity, my approach to the problem, and the basic concepts in data science (EDA, visualization, model training, ... ).

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
    - XGB classifier

### **References** 
* [**Scikit-learn**, Semi-Supervised.](https://scikit-learn.org/stable/modules/semi_supervised.html#label-propagation)
* [**Thomas Kipf**, GRAPH CONVOLUTIONAL NETWORKS.](http://tkipf.github.io/graph-convolutional-networks/)
* [**Gowri Shankar**, Graph Convolution Network - A Practical Implementation of Vertex Classifier and it's Mathematical Basis](https://gowrishankar.info/blog/graph-convolution-network-a-practical-implementation-of-vertex-classifier-and-its-mathematical-basis/#graph-nn-classifier)
* [**Xing Li, Wei Wei, Xiangnan Feng, Xue Liu, Zhiming Zheng**,Representation Learning of Graphs
Using Graph Convolutional Multilayer
Networks Based on Motifs](https://arxiv.org/abs/1609.02907)

### **Future steps**
* Try to build the graph with **jraph**, a lightweight library for working with **GNNs** in **JAX**.
## Specification 

- Windows 11
- python version : 3.7.13
- RAM : 16 GB
- CPU : Intel i5-9300H CPU @ 2.40GHz   2.40 GHz
- GPU : NVIDIA GeForce RTX 2060

### My sincere appreciation to **Bigmama Technology** for this challange.

### Author : **Ramy HAFDI**.