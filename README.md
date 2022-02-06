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

## 4. Data

<p align = "justify"> The data that will be used is from Gaia Early Data Release 3 (Gaia eDR3, Gaia Collaboration 2016b; 2020a). The third early data release (eDR3, Gaia Collaboration et al. 2018) of the ESA Gaia space mission (Gaia Collaboration et al. 2016b) is by far the deepest and most precise astrometric catalogue ever obtained, with proper motion nominal uncertainties a hundred times smaller than UCAC4 and PPMXL. 
</p>

<p align = "justify"> We download sources from Gaia eDR3 in a cone around the cluster centre for a value of radius that is greater than the tidal radius of the cluster. Though our algorithm is quite robust to the choice of this initial radius, we download sources within a radius of 180 arcmin from the cluster centre. Next, we select the sources that satisfy the following criteria (Agarwal et al. 2021):
<ol type="1">
<li>Each source must have the five astrometric parameters, positions, proper motions, and parallax as well as valid measurements in the three photometric passbands G, GBP, and GRP in the Gaia eDR3 catalogue.</li>
<li>Their parallax values must be non-negative.</li>
<li>To eliminate sources with high uncertainty while still retaining a fraction of sources down to G ∼ 21 mag, the errors in their G-mag must be less than 0.005.</li>
</ol>
</p>

You can download NGC 752 data [here](https://drive.google.com/file/d/1krYBlajvirNH5L_1GXfxUIxbeMZoKpUT/view?usp=sharing).

