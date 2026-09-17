# CCRNet: Error-Supervised State-Conditioned Progressive Reconstruction for RGB-Guided Depth Super-Resolution


This repository provides the official implementation of:

**CCRNet: Error-Supervised State-Conditioned Progressive Reconstruction for RGB-Guided Depth Super-Resolution**


## Introduction

RGB-guided depth super-resolution (DSR) aims to reconstruct a high-resolution depth map from a low-resolution depth observation with the assistance of a paired RGB image.

However, RGB appearance is not always consistent with depth geometry. Texture, illumination, and material boundaries may introduce misleading guidance, while reconstruction errors can propagate through progressive refinement.

To address these challenges, we propose **CCRNet**, an error-supervised state-conditioned framework that regulates progressive reconstruction according to the current reconstruction condition.


## Method

CCRNet consists of three key components:

- **Reliability-Guided Initialization (RGI)**  
  Estimates RGB-guidance structural reliability to suppress unreliable RGB information.

- **Agreement-Calibrated Bridge (ACB)**  
  Constructs a compact reconstruction state using:
  - depth structural evidence
  - reconstruction risk
  - RGB-depth structural agreement

  and performs state-conditioned residual transition.

- **Reliability-Gated Refinement (RGR)**  
  Performs final risk-aware residual correction.


## Results

CCRNet achieves competitive performance on RGB-guided depth super-resolution benchmarks.

### NYU-v2

| Scale | RMSE (cm) |
|---|---|
| ×4 | 1.09 |
| ×8 | 2.30 |
| ×16 | 4.33 |


## Dataset

Experiments are conducted on:

- NYU-v2
- Middlebury
- Lu
- RGB-D-D


## Pretrained Models

Pretrained models will be released soon.
