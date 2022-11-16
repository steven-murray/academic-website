---
title: 21cmMC
summary: |
  21cmMC uses [21cmFAST](/codes/21cmFAST) to compare observations with theory, and predict 
  astrophysical and cosmological parameters. This is a beast of a process, since it must run thousands of 
  cosmological simulations to generate the predictions. Thus, 21cmMC is highly parallelized 
  with MPI and is geared to run on supercomputers.

  21cmMC was originally written by [Brad Greig](https://github.com/BradGreig).
  My primary role has been to integrate it with 21cmFAST v3+,
  and to improve the interface and extensibility.

tags:
  - Theory
  - Code
  - Cosmic Dawn
  - EoR
  - Collaborative
date: '2022-09-27T00:00:00Z'

# Optional external URL for project (replaces project detail page).
external_link: 'https://github.com/21cmFAST/21cmMC'

image:
  # caption: Photo by rawpixel on Unsplash
  focal_point: Smart

links:
  - icon: github
    icon_pack: fab
    #name: Follow
    url: https://github.com/21cmFAST/21cmMC
  # - icon: arrow-up-right-from-square
  #   icon_pack: fas
  #   #name: Follow
  #   url: http://homepage.sns.it/mesinger/DexM___21cmFAST.html
url_code: ''
url_pdf: ''
url_slides: ''
url_video: ''
---


21cmFAST is the premiere semi-numerical 21cm cosmological simulator. It is currently 
used by every 21cm cosmology experiment to derive predictions of the spatial distribution 
of 21cm brightness temperature, to compare to observations.

I am a core developer in this project. My role has been primarily to wrap the fast C-code 
of the original simulator into Python, so that it can be more widely 
and easily used. This also has the benefit of adding a number of tests so that future
development is safer and so that the code can be trusted by its many users.
