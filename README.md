# open-cluster-with-DBSCAN

<p align = "justify">  In this project, we will determine the cluster members of an open cluster using Hierarchical Density-Based Spatial Clustering of Applications with Noise (HDBSCAN). The open cluster data that will be used is NGC 752 from Gaia Early Data Release 3 (eDR3). </p> 

## 1. Introduction

<p align = "justify"> Open clusters have long been regarded as powerful tools for studies of the Galactic disk and evolution of stars (Chen, 2003). Membership determination is the first step to study an open cluster, which can directly influence estimation of physical parameters. Various methods have been used for membership determination based on proper motions, radial velocities, photometric data and their combination.
</p>
<p align = "justify"> Various algorithms have been developed for the determination of star cluster membership. Machine-learning applications for this case were introduced such as DBSCAN (Gao, 2014), Gaussian Mixture Model (Gao, 2020), KMEANS (El Aziz et al. 2016), k-th nearest neighbor (Gao, 2016), ML-MOC (Agarwal et al. 2021) and many more.
</p>

## 2. Objectives

<p align = "justify"> Aims of the workshop is to determine the membership of open cluster.</li> 
</ol>
</p>

## 3. (Verry Short) Theoretical Background

<p align = "justify"> Hierarchical Density-Based Spatial Clustering of Applications with Noise (HDBSCAN) is a natural evolution of DBSCAN released in the past few years, almost 20 years after DBSCAN (Ester et al. 1996). DBSCAN identifies clusters as overdensities in a multi-dimensional space in which the number of sources exceeds the required minimum number of points within a neighborhood (minPts) of a particular linking length ε. </p>

<p align = "justify"> HDBSCAN works in a similar way except the user only needs to set a minimum cluster size. It does not depend on ε; instead it condenses the minimum spanning tree by pruning off the nodes that do not meet the minimum number of sources in a cluster, and reanalyzing the nodes that do (Kounkel & Covey, 2019). Not only does it automatically determine other things to set a density threshold accurately, it also does this on local levels, meaning that clusters can be returned in different areas of a dataset with different density levels. </p>

