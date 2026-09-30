---
title: An End-to-End Numerical Framework for Tidal Disruption Events with AthenaK
authors:
  - Hongxuan Jiang
  - Mengqi Yang
  - David A. Velasco-Romero
  - Fangyuan Yu
  - Jing-ze Xia
  - me
  - Yosuke Mizuno
author_notes:
  - ""
date: 2026-09-30T12:14:00.429Z
publishDate: 2026-09-30T12:14:00.429Z
publication_types:
  - article-journal
publication: arXiv
publication_short: ""
abstract: >
  In a tidal disruption event (TDE), a star is torn apart by the tidal field of
  a black hole (BH), and its bound debris returns over many orbits to form an
  accretion disk. We present a framework built on the GPU-accelerated
  finite-volume code AthenaK that follows these stages in a single simulation
  with self-gravity throughout. We extend AthenaK with a moving simulation
  frame, restart remapping between domains, a multigrid Poisson solver on the
  adaptive mesh, a tabulated hydrogen-helium equation of state including
  recombination, a dual-energy update for the cold supersonic debris stream, a
  moving BH potential with excision, and localized adaptive time stepping (LAT),
  in which each MeshBlock advances on its own timestep, speeding up the
  production calculation by more than a factor of three. Each component is
  validated separately and in combination. The gravity solver maintains an
  isolated Lane-Emden sphere to a radial density error of 2.0e-3 over 16.3
  dynamical times, and dual-energy recovery reduces the pressure error of a Mach
  7.75e7 entropy wave from 15.7 to 4.0e-12. We demonstrate the framework with a
  Newtonian beta=1 disruption of a 1 Msun, 1 Rsun star by a 10^3 Msun BH. The
  debris has the expected energy spread, which is insensitive to the
  self-gravity update interval, splits evenly into bound and unbound material,
  and yields a fallback rate that approaches t^(-5/3) at late times. At the
  pericenter nozzle, the thermal energy gained in the high-resolution run
  matches the vertical kinetic energy lost to within 5%, whereas the fiducial
  run (4x lower resolution in x,y and 8x in z) suffers from excessive numerical
  dissipation that overheats the thinnest early stream. The heating in the two
  runs agrees to 12% once the returning stream has thickened. Multifrequency LTE
  post-processing turns the snapshots into synthetic images and luminosities.
summary: null
tags:
  - Research
  - Black Hole
featured: false
hugoblox:
  ids:
    arxiv: "2608.29365"
links:
  - type: link
    url: "https://scixplorer.org/abs/2026arXiv260829365J/abstract"
image:
  caption: "Image credit: [**Unsplash**](https://unsplash.com)"
  focal_point: ""
  preview_only: false
projects: []
slides: ""
draft: false

---

<!-- Add the paper text or supplementary notes. Markdown, math, and code are supported. -->
