---
title: Nested State Clouds: Distilling Knowledge Graphs from Contextual Embeddings
authors: Paul Bricman
year: 2022
zotero: zotero://select/items/@bricmanNestedStateClouds2022
---
#literature

**Nested State Clouds: Distilling Knowledge Graphs from Contextual Embeddings**

Get a sparse knowledge graph/nested state cloud/abstraction hierarchy from a ML model’s high-dimensional embeddings (output vector of vector-embedding model (e.g. word2vec)).

Idea: 
-   Create a matrix where columns are single BERT output vectors, one matrix for one concept/word (every column is an occurrence of that concept in the dataset), and make a conceptor from that. 
-   Define abstraction order of these conceptors using mean eigenvalue of difference matrix (diff. of conceptors). 
-   Create an abstraction graph using Simulated Annealing, where this order score is used in the cost function of the local search. Also take into account the no. of arcs, children & parents of nodes.     

Results: Works, but effectively a proof of concept. Only works w/ menonymous relation is_a, is not scalable really, doesn’t take into account that identical symbols can represent different concepts, etc etc etc.