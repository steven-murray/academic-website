---
title: "matvis: a matrix-based visibility simulator for fast forward modelling of many-element 21 cm arrays"
authors:
- steven
date: "2025-01-10T00:00:00Z"
ids:
  doi: "10.1093/rasti/rzaf001"

# Schedule page publish date (NOT publication's date).
# publishDate: "2017-01-01T00:00:00Z"

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ["2"]

# Publication name and optional abbreviated publication name.
publication: "Royal Astronomical Society Techniques and Instruments"
publication_short: "RASTI"



# Summary. An optional shortened abstract.
summary: |
  We introduce matvis, a GPU-accelerated matrix-based visibility simulator for 
  many-element 21 cm arrays that allows simulation of mock observations on unprecedented
  scales.

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
  - icon: brands/github
    type: code
    url: https://github.com/hera-team/matvis
  - type: pdf
    url: https://academic.oup.com/rasti/article-pdf/doi/10.1093/rasti/rzaf001/61413923/rzaf001.pdf
  - type: link
    url: https://doi.org/10.1093/rasti/rzaf001

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

# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
# slides: example
---



## A faster way to connect models of the radio sky to interferometric observations

<span class="__dimensions_badge_embed__" data-doi="10.1093/rasti/rzaf001" data-style="small_circle"></span><script async src="https://badge.dimensions.ai/badge.js" charset="utf-8"></script>

Radio interferometers like HERA and the SKA don't "see" the sky directly like we imagine
with optical telescopes. Instead, they measure something called "visibilities", which are
complex-valued correlations between pairs of antennas. To interpret these visibilities in
terms of the underlying astrophysics, we need to simulate what visibilities would be
measured for a given model of the radio sky. This process is called "forward modelling",
and it's essential for connecting theoretical models to real data.

However, simulating visibilities for modern arrays with huge numbers of antennas (350 
for HERA, 512 for the SKA!) is computationally challenging. Since visibilities are measured
for each *pair* of antennas, the number of visibilities scales as the square of the number of antennas.
This makes traditional simulation methods slow and resource-intensive, limiting our ability
to explore large parameter spaces or generate many mock observations.


## What is matvis?

[matvis]({{< relref "/software/matvis" >}}) is a new GPU-accelerated matrix-based 
visibility simulator for many-element 21 cm arrays that opens up the possibility of 
simulating mock observations on unprecedented scales.
Fundamental to matvis is a reformulation of the visibility simulation problem in terms of matrix
operations, which can be executed extremely efficiently on modern GPUs. By leveraging the
parallel processing power of GPUs and optimizing memory usage, matvis achieves significant
speed-ups (more than a thousand-fold!) compared to traditional CPU-based methods.

## What did we do in this work?

In this paper, we introduce matvis and demonstrate that despite its speed, it produces
accurate visibility simulations. We validate matvis against traditional simulation methods,
showing excellent agreement in a variety of test cases. We also showcase matvis's ability to
simulate visibilities for large arrays like HERA and the SKA in a fraction of the time
required by traditional methods.

## Who can use matvis?

matvis is open-source and freely available to the community! You can find the code
on [GitHub]({{< relref "/software/matvis" >}}), along with documentation and examples to 
help you get started. While matvis was developed by the HERA collaboration, it is not
specific to HERA and can be used for simulating visibilities for any many-element
21 cm array -- including those that are not focused on 21 cm cosmology.
Importantly, matvis is included in the list of supported simulators
for the [hera_sim]({{< relref "/software/hera_sim" >}}) package, making it easy to integrate
into existing workflows for simulating HERA observations.

## What's next?

Looking ahead, we plan to continue developing matvis by adding new features and
improving its performance. For example, in the paper we outline an experimental algorithm that may
improve performance for highly-regular arrays like HERA even further. 

We also hope to see matvis adopted by the broader community for a variety of applications,
which is why we've made it open-source and easy to use. If you're interested in using
matvis for your own work, please check out the Github repository!
