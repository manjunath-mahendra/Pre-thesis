# Pre-thesis
Cluster extraction and annotation strategies on tabular datasets with diverse feature types

Uniform Manifold Approximation and Projection (UMAP) is the commonly used approach to
find the clusters in clinical and epidemiological datasets. For diverse feature types, using only the
Euclidean metric may not reflect or take into consideration the various feature types. To address
this problem Feature-type Distributed Clustering (FDC) has been proposed.
In the original research work proposing FDC, Density-Based Spatial Clustering of Applications
(DBSCAN) was used to extract the clusters from a 5-dimensional embedding(2-dimension from
Continuous features,2-dimension from ordinal features, and 1-dimension from nominal features)
generated by FDC. However, the workflow was largely empirical. The effect of using clustering
algorithms other than DBSCAN remains to be investigated and the effect of extracting clusters
from different embeddings other than the conventional 5-dimensional embedding remains to be
tested. Moreover, whether it is possible to learn the cluster embeddings and labels (that might
be significant in a domain-specific way) in a supervised manner and use the trained model to
automatically annotate the similar clusters in unseen data remains unexplored.
We used a pre-processed part of National Family Health Survey-4 (NFHS-4) data of 10, 125
Type 2 Diabetes Mellitus (T2DM) patients for our analysis. In our study, we trained two neural
networks to annotate the clusters on unseen data. We compared different clustering algorithms
such as DBSCAN, K-means, and agglomerative to extract the clusters. Additionally, we also
used different clustering strategies for extracting clusters from different embeddings other than the
conventional 5-dimensional FDC embedding and compared the results by calculating a measure
Cluster Incidence Score (CIS), which we defined in this work.
Our analysis show that a Neural Network (NN) can learn the cluster embeddings and labels
generated by all clustering strategies we investigated. Moreover, cluster extraction can also be
accomplished using K-means and agglomerative clustering algorithms in addition to DBSCAN.
However, we noticed that automatic annotation of clusters on unseen data is more effective if
we use the DBSCAN algorithm to extract clusters from a special 3-dimensional FDC embedding
proposed in this work. Moreover, this also reduces the number of data points annotated as noise
by the DBSCAN algorithm compared to the conventional application of FDC.
Our result implies that, if FDC is used to annotate clusters in some clinical/epidemiological data
then by using supervised models, the same clusters can be automatically annotated and extracted
reliably, in unseen data.
