# README

This directory contains postprocessing data for a transient diffusion problem. We compare performance of ASC(0), ASC(1), arithmetic, and harmonic homogenization methods.

## Description of The Problem

* Continuous:
  * Domain is the unit square, we prescribe Dirichlet data $p \equiv 1$ on the left and right sides; top and bottom sides are insolated 
  * Diffusion tensor $K = k I$, $k = 1, .005, 10$ on the left, middle, and right sandwich layer, respectively
  * $t \in [0, T = 5]$, stationary mode is $p \equiv 1$
* Discrete:
  * We use conformal supermesh (supermesh.png) to get the reference solution with 10 000 and $dt = T / 40$
  * For ASC(0), ASC(1), arithmetic, and harmonic homogenization methods we use $dt = T / 20$ and Voronoi mesh with $h = 8.1 \times 10^{-2}$ (465 base cells)

## What is What

* movie.avi: comparision of all the methods + the difference between ASC(0) and ASC(1). You can see that the difference is not huge: both methods perform well. They both beat homogenization by the "eyeball" norm. *Note:* at $t = .25$ gradient changes rapidly, and the flux is othogonal to the interface; thus I was hoping that ASC(1) beats ASC(0), but turns out ASC(0) stays quite robust; I will add an example with 3 materials later--hopefully, ASC(1) will perform reasonably better
* movie_frames: same story as above but with each time frame as .png, so it is convinient to insert in the paper
* movie_slices.avi, movie_slices_frames, ref_slices.png: same story, but for $y = .5$  

*Sasha*
