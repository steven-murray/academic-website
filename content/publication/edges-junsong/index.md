---
title: "The EDGES measurement disfavors an excess radio background during the cosmic dawn"
authors:
- steven
date: "2025-06-10T00:00:00Z"
ids:
  doi: "10.1051/0004-6361/202452982"

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
  We re-analyze the same EDGES data that sparked a rush of interest in exotic dark matter
  models and excess radio backgrounds, finding that accounting for both the possibility 
  of small instrumental effects and more accurate physical priors, *disfavors*
  the presence of an excess radio background during the cosmic dawn.

tags:
- Cosmic Dawn
- MSCA
- Theory
  
featured: true

# links:
# - name: ""
#   url: ""
links:
  - type: pdf
    url: https://www.aanda.org/articles/aa/pdf/2025/06/aa52982-24.pdf
  - type: link
    url: https://doi.org/10.1051/0004-6361/202452982

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



## Revisiting the EDGES low-band measurement

<span class="__dimensions_badge_embed__" data-doi="10.1051/0004-6361/202452982" data-style="small_circle"></span><script async src="https://badge.dimensions.ai/badge.js" charset="utf-8"></script>

The Experiment to Detect the Global Epoch of Reionization Signature (EDGES)
collaboration made headlines in 2018 when they reported the detection of an
unexpectedly deep 21 cm absorption feature centered at 78 MHz in their (I suppose I 
should say "our" now, though I joined the collaboration after this result was 
published) low-band data. This result sparked a flurry of theoretical activity, 
as the depth of the absorption feature was more than twice as large as the maximum
allowed by standard astrophysical models. To explain this discrepancy, theorists
proposed a variety of exotic scenarios, including interactions between dark matter
and baryons, as well as the presence of an excess radio background beyond the
cosmic microwave background (CMB) at these redshifts.

However, most of the physical models proposed to explain the EDGES result
focused on reproducing the depth of the absorption feature, without
fully accounting for the detailed shape of the measured spectrum.
In this work, we re-analyze the same EDGES low-band data, but with three key
improvements over previous analyses. First, we account for the possibility of
small instrumental systematics that could affect the measured spectrum 
(similar to [Peter Sims' excellent 2019 paper](https://arxiv.org/pdf/1910.03165)). 
Second, we use the full data spectrum, simultaneously fitting for the foregrounds,
instrumental effects, and 21 cm signal, rather than just focusing on matching the
depth of the absorption feature. Finally, we use a new physically-motivated model 
that self-consistently allows for excess-radio-background scenarios at high redshift 
while naturally "turning off" the excess background at low redshift to match existing
observational constraints.


## Surprising results: no evidence for an excess radio background

Contrary to previous interpretations of the EDGES result, we find that when
accounting for possible instrumental systematics and using a more accurate
physical model, the data do not favor the presence of an excess radio background
during the cosmic dawn. In fact, our analysis disfavors such scenarios at high
statistical significance.

Instead we find that the EDGES data prefer models with standard astrophysics
and no excess radio background, with a low but non-zero level of residual systematics. 

## Why did we reach different conclusions?

When we fit our more physically-motivated model directly to the best-fit 
absorption profile reported by EDGES, we do find that an excess radio background
is required to match the depth of the feature. However, this common approach
neglects the interplay of foregrounds, instrumental effects, and the 21 cm signal.
When simultaneously fitting for all of these components to the raw data, we find 
the opposite conclusion: the data do not favor an excess radio background. This highlights
the importance of using principle Bayesian inference methods and accurate physical models
when interpreting global 21 cm measurements.

Our investigation suggests that the primary factor driving the favoured models away
from excess radio backgrounds is the *shape* of the measured spectrum, rather than
the depth of the absorption feature alone. The extremely sharp evolution in the
absorption profile reported by EDGES is difficult to reconcile with physical models that
must evolve smoothly over cosmic time. This tension is alleviated in our analysis by allowing for
small instrumental systematics, which can mimic sharp features in the spectrum. However,
once these systematics are accounted for, the data no longer require an excess radio background
at all.

## What's next?

Our results depend on the assumption that the small instrumental systematics we model
are indeed present in the EDGES data. Future work should aim to better understand
the instrument and its calibration to confirm or refute this assumption. 

In the meantime, the next-generation version of the EDGES instrument, EDGES-3,
is currently taking data with improved design and calibration techniques.
We eagerly await results from EDGES-3, which will provide a fresh opportunity to
probe the global 21 cm signal during the cosmic dawn and test the conclusions
of this work.