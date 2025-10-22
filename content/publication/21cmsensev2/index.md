---
title: "21cmSense v2: A modular open-source 21 cm sensitivity calculator"
authors:
- steven
date: "2024-05-09T00:00:00Z"
ids:
  doi: "10.21105/joss.06501"

# Schedule page publish date (NOT publication's date).
# publishDate: "2017-01-01T00:00:00Z"

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ["2"]

# Publication name and optional abbreviated publication name.
publication: "Journal of Open Source Software"
publication_short: "JOSS"

#abstract: |
  # We develop a Bayesian model that jointly constrains receiver calibration, foregrounds, and cosmic 21 cm signal for the EDGES global 21 cm experiment. This model simultaneously describes calibration data taken in the lab along with sky-data taken with the EDGES low-band antenna. We apply our model to the same data (both sky and calibration) used to report evidence for the first star formation in 2018. We find that receiver calibration does not contribute a significant uncertainty to the inferred cosmic signal (⁠<1 per cent⁠), though our joint model is able to more robustly estimate the cosmic signal for foreground models that are otherwise too inflexible to describe the sky data. We identify the presence of a significant systematic in the calibration data, which is largely avoided in our analysis, but must be examined more closely in future work. Our likelihood provides a foundation for future analyses in which other instrumental systematics, such as beam corrections and reflection parameters, may be added in a modular manner.

# Summary. An optional shortened abstract.
summary: A new method for computing the power of 21cm experiments to detect the cosmological 21cm signal.

tags:
- EoR
- Cosmic Dawn
- MSCA
  
featured: true

# links:
# - name: ""
#   url: ""
links:
  - type: site
    url: https://21cmsense.readthedocs.io/en/latest/
  - icon: github
    icon_pack: fab
    url: https://github.com/rasg-affiliates/21cmSense
  - type: pdf
    url: https://www.theoj.org/joss-papers/joss.06501/10.21105.joss.06501.pdf

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

[21cm cosmology]({{< relref "/post/cosmic-dawn" >}}) promises a direct view into the 
first billion years of cosmic history. Instead of light from stars and galaxies, 21cm experiments listen for the faint radio glow of the neutral hydrogen that surrounds the first stars and galaxies, at 21-centimetre wavelengths. 
Turning those whispers into science requires careful planning: which telescope layouts, observing times, and analysis choices will actually deliver a robust detection? That's where 21cmSense v2 comes in — a lightweight, well-documented toolkit that predict how sensitive a given radio array will be to the 21cm signal.

21cmSense v2 builds on earlier tools (21cmSense v1!) by streamlining sensitivity forecasts for interferometric arrays. It takes in straightforward inputs — array configuration, observing time, frequency setup, foreground treatment and noise assumptions — and produces quantitative estimates of detectability for power-spectrum measurements. The result is an easy way to compare instrument designs, test how observing strategies change outcomes, and investigate how different sources of uncertainty (telecope noise, and the uncertainty associated with our choice of which part of the Universe to observe, called *cosmic variance*) affect the science reach. For people designing experiments or preparing proposals, that kind of rapid, reproducible forecasting is invaluable.

Why predict sensitivity? Building and operating 21cm experiments is expensive and 
technically demanding. Decisions about antenna placement, total collecting area, bandwidth, or the balance between survey depth and sky coverage can make large differences in how much the observations tell us about astrophysics. 
Sensitivity forecasts help teams prioritize design choices, justify funding, and estimate how long observations will need to run. They also guide data-analysis choices: a forecast can reveal which Fourier modes an experiment can realistically access and where foregrounds or instrumental systematics will dominate, steering developers toward strategies that maximize discovery potential.

Open-source code matters. 21cmSense v2 is openly available and documented in a community-friendly way, so anyone can inspect the assumptions, reproduce results, and extend the code for new instruments or science cases. That transparency builds trust in forecasts used in proposals and papers. It also speeds progress: students can learn the nuts and bolts of sensitivity estimation, instrument teams can adapt the code to unique hardware, and theorists can test how different cosmological signals would show up in realistic observations. Open code reduces duplication of effort and helps the field converge on best practices for forecasting and validation.

If you want to read the formal description and cite the tool, see the JOSS paper: 
https://joss.theoj.org/papers/10.21105/joss.06501.




