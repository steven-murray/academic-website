---
title: "21cmEMU: an emulator of 21cmFAST summary observables"
authors:
- steven
date: "2024-02-10T00:00:00Z"
ids:
  doi: "10.1093/mnras/stad3849"

# Schedule page publish date (NOT publication's date).
# publishDate: "2017-01-01T00:00:00Z"

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ["2"]

# Publication name and optional abbreviated publication name.
publication: "Monthly Notices of the Royal Astronomical Society"
publication_short: "MNRAS"



# Summary. An optional shortened abstract.
summary: |
  We present 21cmEMU, a machine learning-based emulator of the popular 21cmFAST
  simulation code. 21cmEMU can rapidly generate predictions for summary observables
  like the global 21 cm signal and the 21 cm power spectrum, enabling fast parameter
  inference and forecasting for upcoming experiments.

tags:
- Cosmic Dawn
- Machine Learning
- MSCA
- Theory
  
featured: true

links:
  - type: pdf
    url: https://arxiv.org/pdf/2309.05697
  - type: link
    url: https://doi.org/10.1093/mnras/stad3849

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
  - edges
  - 21cmfast

# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
# slides: example
---



## Speeding up 21 cm inference with machine learning

<span class="__dimensions_badge_embed__" data-doi="10.1093/mnras/stad3849" data-style="small_circle"></span><script async src="https://badge.dimensions.ai/badge.js" charset="utf-8"></script>

Even though we make [21cmfast]({{< ref "/project/21cmfast" >}}) as fast as possible,
creating full 3D simulations of the Universe tens of thousands of times to infer the
astrophysical parameters governing the cosmic dawn and epoch of reionization is still
a pretty big lift. 
One inference run can take weeks on a supercomputer, which limits our ability to
explore new models.
What's more, it's pretty common for us to want to constrain the same model for different
combinations of data. For example, we might want to see how our constraints change when
we add in a new observation, or swap out one dataset for another.
Re-running the full inference for each new combination of data is simply not feasible.

To get around this problem, we've developed [21cmEMU](https://github.com/21cmfast/21cmemu),
a machine learning-based emulator of 21cmfast summary observables like the global 21 cm
signal and the 21 cm power spectrum.
21cmEMU uses neural networks to learn the mapping from astrophysical parameters
to summary observables, allowing it to generate predictions in milliseconds instead
of hours. While it requires an initial investment of time to produce a "training set"
of simulations, once this is done, 21cmemu can quickly provide predictions for new
combinations of parameters or datasets.

This allows us to ask important questions like "what is this particular piece of data
adding to our knowledge?". It is also hugely beneficial for generating forecasts for
upcoming experiments, which often require exploring a wide range of models and scenarios.

While several emulators of 21 cm observables have been developed in the past,
21cmEMU is the first to directly emulate 21cmFAST, the most widely used simulation
code for 21 cm cosmology. It is also the first to simultaneously emulate a range of
summary observables, including the global signal and power spectrum at multiple redshifts,
as well as the electron scattering optical depth, mean neutral fraction history, and
UV luminosity functions. This makes it uniquely powerful for parameter inference, which
requires all of these observables to provide meaningful constraints.

## What's next?

This work was led by Daniela Breitman as part of her PhD thesis.
We continue to collaborate on new ways to incorporate machine learning into 21 cm cosmology,
including improving the accuracy and flexibility of 21cmEMU itself.
