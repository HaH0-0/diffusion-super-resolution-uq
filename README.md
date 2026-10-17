# Uncertainty Quantification for Super-Resolution with Diffusion Priors

**Ka Nam Lam · University of Bristol**  
Undergraduate Research Report · March 2, 2026  
Academic supervisor: Dr. Rihuan Ke

[Read the report (PDF)](UQ_for_SR_using_diffusion_based_priors.pdf)

## Overview

This report examines whether stochastic reconstructions from diffusion-based super-resolution solvers provide calibrated uncertainty estimates.

The study evaluates DDRM and compares it with FPS-SMC, a posterior-targeting sequential Monte Carlo method, on bicubic super-resolution using 200 ImageNet images. DDRM is evaluated at 4× and 8× scale factors, with and without measurement noise; FPS-SMC is evaluated in the noisy settings. Repeated reconstructions use the same measurement for each image.

Evaluation covers sample-mean accuracy, marginal uncertainty calibration, interval sharpness, error localisation, and frequency-based uncertainty diagnostics.

## Main observations

Under the tested sampling settings:

- Both solvers exhibit substantial marginal under-coverage.
- Variance maps retain useful information about the spatial distribution of reconstruction errors.
- The mean frequency under-exploration ratio is below 1 in every evaluated setting, indicating that uncertainty assigns relatively less high-frequency energy than reconstruction error.

These findings concern the reported experiments with finite sampling budgets and 20 reverse diffusion steps. The frequency diagnostic is a proxy for uncertainty allocation, rather than a test of the full joint posterior.

## Repository contents

This repository contains the original report PDF and this overview. It does not include implementation code, datasets, or model weights.

This is an undergraduate research report, not a peer-reviewed publication.
