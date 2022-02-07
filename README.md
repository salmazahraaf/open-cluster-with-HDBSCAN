# open-cluster-with-HDBSCAN

<p align = "justify"> Holla! This project is one of the International Virtual Course Astrostatistics and Machine Learning modules on August 2nd-13th, 2022. In this project, we will determine the cluster members of an open cluster using Hierarchical Density-Based Spatial Clustering of Applications with Noise (HDBSCAN). The open cluster data that will be used is NGC 752 from Gaia Early Data Release 3 (eDR3).
</p> 

<p align = "justify"> The open cluster data I used in this work were downloaded from the Gaia Archive using the attached syntax in the adql-open-cluster file. You can freely replace the data with other open cluster data. To increase data accuracy, you can adjust some additional filters, such as parallax over error whose data has been provided by Gaia. </p> 

<p align = "justify"> Pleas note, our membership assignment relies on the astrometric solution, and we only used the Gaia eDR3 photometry to manually confirm that the groups identified matched the expected aspect of a cluster in a color-magnitude diagram.
</p>

To determine the membership of open cluster NGC 752, we will use a module in python called [hdbscan](https://hdbscan.readthedocs.io/en/latest/) (McInnes et al. 2017). Make sure your machine has installed all the packages needed to run this project.
