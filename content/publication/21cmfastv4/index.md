---
title: "Efficient simulation of discrete galaxy populations and associated radiation fields over the first billion years "
authors:
- steven
date: "2025-09-01T00:00:00Z"
ids:
  doi: "10.1051/0004-6361/202554951"

# Schedule page publish date (NOT publication's date).
# publishDate: "2017-01-01T00:00:00Z"

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ["2"]

# Publication name and optional abbreviated publication name.
publication: "Astronomy & Astrophysics"
publication_short: "A&A"



# Summary. An optional shortened abstract.
summary: |
  A new physical model within the popular 21cmFAST simulation code that allows for the
  efficient generation of discrete galaxy populations and their associated radiation fields,
  over the first billion years of cosmic history.

tags:
- EoR
- Cosmic Dawn
- MSCA
- Theory
  
featured: true

# links:
# - name: ""
#   url: ""
links:
  - type: code
    url: https://21cmfast.readthedocs.io/en/latest/
  - icon: brands/github
    type: code
    url: https://github.com/rasg-affiliates/21cmSense
  - type: pdf
    url: https://arxiv.org/pdf/2504.17254
  - type: link
    url: https://doi.org/10.1051/0004-6361/202554951

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder. 
image:
  # caption: 'Image credit: [**Unsplash**](https://unsplash.com/photos/jdD8gXaTZsc)'
  focal_point: "Smart"
  preview_only: false

# Associated Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `internal-project` references `content/project/internal-project/index.md`.
#   Otherwise, set `projects: []`.
projects:
  - forward
  - 21cmfast

# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
# slides: example
---



## Introducing discrete galaxies into fast reionization simulations

<span class="__dimensions_badge_embed__" data-doi="10.1051/0004-6361/202554951" data-style="small_circle"></span><script async src="https://badge.dimensions.ai/badge.js" charset="utf-8"></script>

Our new paper updates [21cmFAST]({{< relref "/software/21cmfast" >}}) with a fast, 
flexible way to generate realistic, discrete galaxy populations and their radiation 
fields across the first billion years of cosmic history. 

## What is 21cmFAST?

[21cmFAST]({{< relref "/software/21cmfast" >}}) is the most widely used simulation 
code for modeling the 21-cm signal from the Cosmic Dawn and Epoch of Reionization. 
Simulations allow us to connect theoretical models of early galaxy formation to 
observations from current and upcoming radio telescopes like HERA and the SKA: that is,
to be able to interpret that next-generation data in terms of the astrophysics we care about!
In a nutshell, traditional "semi-numerical" simulations like 21cmFAST construct a 3D
grid that represents a large volume (a 'box') of the early Universe, and then use 
approximate but efficient algorithms to predict the density, temperature, ionization, and
21-cm brightness for each cell in that box over time. The speed of these simulations
makes them ideal for exploring large parameter spaces and generating mock observations
(like we did [here](https://arxiv.org/abs/2210.04912) and [here](https://arxiv.org/abs/2108.07282)).

## Why this paper matters

As we just mentioned, most semi-numeric reionization and Cosmic Dawn simulations 
approximate sources by computing the total emissivity inside each simulation cell. 
That’s efficient, but it neglects some important things:
in reality the number of galaxies in each simulation cell is random---even if you know
the *average* number of galaxies expected in that cell (given its density), the actual 
number can vary. This effect is sometimes referred to as "stochasticity" or "shot noise",
and--as shown in [Ivan Nikolic's excellent paper](https://arxiv.org/abs/2406.15237)--
it can have a sizeable impact on predictions for the 21-cm signal.

Another important consideration is that the 21cm signal is not the *only* signal we care
about from the early Universe. Emission at other wavelengths (e.g. Lyman-alpha) can also
be observed, not with radio telescopes but with space-based infrared observatories like
the JWST. Both the 21cm signal and these other signals are driven by the same underlying galaxy
populations, so to make consistent predictions across multiple observables (like we did
[here](https://arxiv.org/abs/2202.08957) and [here](https://arxiv.org/abs/2502.20447)) 
we need to model the galaxies themselves, not just their average emissivity.

This paper introduces a new technique to 21cmFAST that addresses these issues by explicitly
modeling discrete galaxies in the simulation volume. 

## What’s new in the method

Instead of treating emissivity as a continuous field per cell, we sample a dark-matter halo
population consistent with the underlying density in each simulation cell, and the 
[halo mass function]({{< relref "/software/hmf" >}}), assign physical
properties to individual halos (e.g. star-formation rate and X-ray emissivity), and 
compute radiation fields from these discrete sources.
A key advance is the mechanism that correlates halo populations over cosmic time 
(equivalently, over redshift). Real structure formation is continuous: halos grow, merge, 
and the same density peaks tend to host successive generations of halos. The paper 
introduces a practical algorithm that preserves temporal correlations in the halo 
population so that halos at nearby redshifts are not independent random draws. This 
avoids unphysical temporal noise in source counts and radiation fields and produces 
smoother, physically motivated evolution of observables (lightcones, power spectra, maps).
The correlation mechanism is lightweight and tuned to semi-numeric workflows: it 
captures the relevant memory of the density field and halo bias without the overhead of a full N-body merger tree.

## Speed and a clean API

One of the motivating use-cases for 21cmFAST is running large suites of simulations to 
explore astrophysical parameter space (often within a Bayesian inference loop, for 
example using [21CMMC]({{< relref "/software/21cmMC" >}})).
To run the many thousands of simulations required for these studies, speed is essential.
Despite adding per-halo sampling and time-correlations, our new implementation remains fast. 
In fact, several parts of the code run faster than before, thanks to algorithmic improvements,
while the new features add some overhead that we have optimized carefully.

The updated 21cmFASTv4 also refreshes and modernizes the API, making the new features 
easier to adopt, and making it easier to cleanly define and share the configuration 
files that define a simulation.



