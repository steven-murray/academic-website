---
title: HERA
summary: |
  The **Hydrogen Epoch of Reionization Array** is one of the largest radio
  interferometers in the world, and is looking to map the effects of the first stars,
  galaxies and black holes over the first billion years of the Universe.
  
  I co-lead the [Validation Team](https://github.com/hera-team/hera-validation),
  developing increasingly realistic simulations of our observations at scale. I also
  lead the development of an [interface](https://github.com/hera-team/pspec_likelihood)
  to compute theoretical likelihoods on HERA data.
tags:
  - Experiment
  - Cosmic Dawn
  - EoR
date: '2022-10-27T00:00:00Z'

# Optional external URL for project (replaces project detail page).
external_link: ''

image:
  #caption: Photo by rawpixel on Unsplash
  focal_point: Smart

links:
  - icon: github
    icon_pack: fab
    #name: Follow
    url: https://github.com/hera-team
  - icon: arrow-up-right-from-square
    icon_pack: fas
    #name: Follow
    url: https://reionization.org
# url_code: 'https://github.com/hera-team'
url_pdf: ''
url_slides: ''
url_video: ''

---

The Hydrogen Epoch of Reionization Array (HERA) is an experiment to detect spatial fluctuations of the hydrogen signature during Cosmic Dawn and EoR. Instead of the global average that EDGES takes, HERA can see how the signal varies over the sky — potentially even building a 3D ‘map’ of the temperature! HERA is a mid-size collaboration spanning multiple universities in the US and some in Europe and South Africa. The telescope itself is an array (i.e. multiple low-frequency radio dishes joined together) located in the desert in South Africa.

It is fairly clear that understanding how the signal varies over the sky is going to yield a lot more information than a single average. However, getting this information is also extremely difficult — more dishes are required, more computing power and storage (petabytes!), and more complex models for calibration of all the antennas simultaneously. Indeed, making that ‘map’ currently seems a far-off dream. We are instead focused on a simpler, statistical, detection in the form of a power spectrum. The power spectrum encodes the level of variation there is in the temperature between locations separated by a given scale (i.e. how ‘lumpy’ the temperature distribution is on that scale). Because we expect that variation to be the same in all directions, so long as the scale length itself remains constant, we are able to average up all the directions to make a more sure detection. Thus, the power spectrum is also an averaged detection — just not as averaged as the global experiments!

The different scales are accessed in two ways: firstly, scales ‘perpendicular’ to the line of sight (i.e. scales you’d get by measuring their distance from each other on the sky with your hand) are accessed by correlating the measurements of two separate antennas; the distance between the antennas corresponds in inverse proportion to the perpendicular scale (i.e. halving the distance between antennas doubles the scale they measure on the sky). That’s why an array of antennas is required to understand the spatial fluctuations. Secondly, scales ‘parallel’ to the line of sight (i.e. the distance you’d have to travel in a spaceship to get from one star to another directly behind it, as viewed from Earth) are directly measured by different frequencies (the same as the global experiment).

HERA is currently under construction, though it is taking data with a subset of its antennas. Eventually it will consist of 350 antennas, all tightly packed in a hexagonal shape. The hexagonal shape maximizes the number of pairs of antennas (called baselines) that have the same distance between them (but different orientations). This helps to get lots of measurements of the power spectrum at the same scale and thus lower our eventual uncertainties. Its frequency range is from 50 – 250 MHz, covering the full EDGES range, and a little bit more.

My main task within HERA, which I joined in late 2018, is as co-lead of the validation subgroup. This group is tasked with verifying that the full HERA analysis pipeline does what it says on the tin. The analysis pipeline is an incredibly complex beast, comprising more than 40,000 lines of code over several repositories, developed by different subsets of people. While each stage of the pipeline is tested independently, there is a possibility that when put together, they will interact in ways that subtly introduce errors. The validation team has devised a number of tests that put together multiple parts of the pipeline, and ensure their final output (the power spectrum) matches a known simulated input power spectrum. We have also designed a full ‘end-to-end’ test in which a large-scale simulation of the EoR, plus galactic and extra-galactic foregrounds (from the GSM and GLEAM respectively) are input to a full treatment of instrumental systematics using our own hera_sim code: thermal noise, gains, cross-coupling, cable reflections and RFI flags. This tests the full HERA analysis pipeline.

I also write fair bit of code for the HERA project, including for hera-validation, hera_sim and pyradiosky.

Other interferometry-based EoR research interests I have been involved in (not strictly related to HERA) are modelling the point-source (extragalactic) foregrounds, in a way that helps us understand their impact on measured power spectra. Also, I’ve done work on understanding the features of highly regular, compact arrays, similar to the Fast Fourier Transform Telescope. Rather than focusing on computational efficiency, I focus on their ability to create a smooth spectral response, which could mean that we can pull a lot more information out of our power spectra than we could previously (for the initiated: we can substantially mitigate the ‘foreground wedge’). 


