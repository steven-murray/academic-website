---
title: hankel
summary: |
  A small Python code that implements a way to do a very specific integral 
  transform — the Hankel transform.

  This transform is particularly common in astrophysics and cosmology (for instance, it is 
  required to transform a correlation function into a power spectrum and vice versa). It is 
  also a bit of a tricky integral to do, because it is highly oscillatory. This code 
  implements a [neat idea](https://www.ems-ph.org/journals/show_abstract.php?issn=0034-5318&vol=41&iss=4&rank=8)
  (not mine!) that is able to accurately perform this integral with
  good computational performance (in most cases).

tags:
  - tool
  - mine

date: '2022-09-27T00:00:00Z'

image:
  # caption: Photo by rawpixel on Unsplash
  focal_point: Smart

links:
  - icon: brands/github
    url: https://github.com/steven-murray/hankel
  - icon: academicons/arxiv
    url: https://arxiv.org/abs/1906.01088
    type: pdf

---


