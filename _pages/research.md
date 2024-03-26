---
title: "Research"
permalink: "/research/"
---


My primary interest is in geospatial data. Specifically, I think about spatial
point patterns, how to design sampling plans to observe point pattern data,
and fitting point process models to incompletely-observed point patterns.

At the present, I am not actively pursuing my own academic research.
However, if my work helps you, I would love to hear from you! I am also
interested in peer-reviewing manuscripts.


## Path-Based Sampling Designs

Chapter 4 of my
[dissertation](https://scholarworks.montana.edu/xmlui/handle/1/16040) used a
simulation study to compare several methods of constructing paths to traverse
around a site when data collection is such that all events within a radius of
the path will be observed and all events beyond that radius will be
unobserved. I used a spatial LGCP model fit via INLA and the SPDE approximation
to predict the intensity surface over the site. My conclusion is that paths
with lots of "zigzagging" (_sure to become a popular technical term..._) do a
good job of ensuring that every location in the site is close to some part of
the path and lead to predictions that perform well on most meaningful
performance statistics.

I created a [gallery](https://kflagg.github.io/manuscript2/graphics/) of plots
to help understand the massive volume of simulation output.

My results were plagued with model fits that failed to converge due to poor
choice of finite element mesh. Further investigation of mesh construction is a
natural next step, and I would be happy to guide any researchers wishing to
tackle this.


## Fitting LGCP Models with R-INLA

I wrote a [tutorial](https://doi.org/10.1080/02664763.2021.2023116) on fitting
spatial log-Gaussian Cox process models using with R-INLA and a finite element
(SPDE) approximation. Such models are rather nontrivial to set up and there
was very little documentation available before I wrote this. I released
accompanying [example code](https://github.com/kflagg/jas-inla-review).


## DP Infinite Mixture Models

My first foray into spatial point process models was working with magnetometer
data from unexploded ordnance remediation projects. The sites I focused on were
domestic training/testing ranges where repeated firing at stationary targets
justified a mixture of normally-distributed hotspots. I published a study using
a [Dirichlet process infinite mixture model](https://doi.org/10.1007/s13253-020-00387-2).
Ultimately, the computing time was prohibitively large, and the posterior
mixture contained too many redundant components to be useful (i.e. the model is
prone to overfitting). I recommend the equally useful and computationally
tenable LGCP model instead.

My [R package](https://github.com/kflagg/poisDPmix) for the DP mixture is out
there if you should want to explore it.

