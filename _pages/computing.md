---
title: "Statistical Computing Resources"
permalink: "/computing/"
---


I put in a lot of effort to learn the tools I use, and I want to make it
easier for the next generation.


## Python

While working in business data science, I migrated from R to Python. I began an
ongoing side project (likely never to be finished) to create a curriculum for
people with statistical training to learn to do data analysis in Python. But
certain sections are useful.

- If your exposure to "programming" is instructors providing you with code that
  they themselves barely understand, [Chapter 1](https://kflagg.gitbook.io/pythonds/1.-getting-started-python-setup-how-computers-run-code) will be valuable.
- If you have done some coding in Python and need experience working with
  tabular data, [Chapter 2](https://kflagg.gitbook.io/pythonds/2.-pandas-structuring-data-for-analysis) curates a set of tutorials.
- Similarly, [Chapter 3](https://kflagg.gitbook.io/pythonds/3.-statsmodels-traditional-statistics) will get you starting doing some classical statistics.

Now, if you are a budding data scientist, you will at some point need to ensure
that the code you wrote gets run the exact same way by the exact same version
of every module on every single machine that event runs it. I don't want to
get that deep or technical here, but
[this article](https://realpython.com/intro-to-pyenv/)
on Pyenv is something I have consulted many times.


## R

- Tutorial on [fitting spatial LGCP models](https://doi.org/10.1080/02664763.2021.2023116)
  with R-INLA and a finite element (SPDE) approximation.
  - [Example code](https://github.com/kflagg/jas-inla-review)
- [PoisDPmix](https://github.com/kflagg/poisDPmix), an R package for fitting
  infinite mixtures of Gaussians to partially-observed spatial point pattern
  data.
  - The code and documentation are in a poor state as I do not expect this to
    be useful to anyone, but if you want to use it please let me know!

