# README

(Same setting as in transient example 2 but with a triangular base mesh.)

This directory contains postprocessing data for a transient diffusion problem. We compare performance of ASC(0), ASC(1), arithmetic, and harmonic homogenization methods.

## Description of The Problem

* Continuous:
  * Domain is the unit square, we prescribe Dirichlet data $p \equiv 1$ on the left side; right, top, and bottom sides are insolated 
  * Diffusion tensor $K = k I$, $k = 1, .002, 10$ outside the ring, inside the ring, and in the inner part, respectively
  * $t \in [0, T = 5]$, stationary mode is $p \equiv 1$
* Discrete:
  * We use conformal supermesh (supermesh.png) to get the reference solution with 4 908 triangles and $dt = T / 40$
  * For ASC(0), ASC(1), arithmetic, and harmonic homogenization methods we use $dt = T / 20$ and triangular mesh with $h = 0.125$ (456 base cells)
  * Number of MMCs: 62
  * Number of 3 material faces: 3

## What is What

* movie.avi: comparision of all the methods + the difference between ASC(0) and ASC(1)
* movie_frames: same story as above but with each time frame as .png, so it is convinient to insert in the paper
* movie_slices.avi, movie_slices_frames, ref_slices.png: same story, but for $y = .5$ 
* l2err_cells.png: cells over which we compute discrete l2 norm of $(p - p_h)$
* l2err.png, l2err_1.png: plot of the l2 error norms for all the time frames and methods that were used

*Sasha*
