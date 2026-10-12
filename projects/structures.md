
---
layout: default
title: Aerospace Structures Analysis
---

# Aerospace Structures Analysis

**The University of Alabama | AEM 341 | April 2026**

**Tools:** MATLAB, Excel  
**Methods:** Bernoulli–Euler Beam Theory, Computational Modeling, Experimental Validation

## Project Overview

Developed a MATLAB program to analyze bidirectional bending of an unsymmetrical L-shaped cantilever beam. The project involved calculating structural properties, bending stresses, and horizontal and vertical deflections, followed by comparisons with experimental strain and displacement measurements.

![L-shaped cantilever beam geometry](../images/beam-geometry.png)

*Figure 1. L-shaped cantilever beam geometry and loading configuration.*

## Part 1 — Computational Structural Analysis

Developed a generalized MATLAB model using Bernoulli–Euler beam theory to calculate:

- Centroid location, area moments of inertia, and product of inertia.
- Neutral-axis orientation and bending moments.
- Bending stresses at specified strain-gage locations.
- Horizontal and vertical beam deflections.

The model was applied to a 1-meter aluminum cantilever beam subjected to a 12-lb tip load.

The analysis demonstrated coupled horizontal and vertical deflection due to the unsymmetrical cross-section.

![Horizontal and vertical beam deflections](../images/beam-deflections.png)

*Figure 2. Predicted horizontal and vertical beam deflections from the MATLAB model.*

## Part 2 — Experimental Comparison and Model Refinement

Extended the MATLAB model to compare theoretical predictions against experimental strain and deflection measurements from AEM 351.

The initial model assumed a nominal Young's modulus of 68.9 GPa and perfect clamping.

To improve agreement with experimental measurements, I evaluated:

- A fitted Young's modulus.
- Non-ideal clamping boundary conditions.
- A combined fitting approach involving both parameters.

![Theoretical and experimental comparison](../images/model-validation.png)

*Figure 3. Comparison of theoretical and experimental results using fitted material properties and boundary conditions.*

## Key Results

- Baseline vertical displacement RMSE: 10.097 mm.
- Fitted-boundary vertical displacement RMSE: 1.1339 mm.
- Combined-fit vertical displacement RMSE: 0.88417 mm.
- The combined-fit model provided the best overall compromise between the measured strain and displacement responses.

## Engineering Takeaways

The project demonstrated how assumptions about material properties and support conditions can influence structural predictions.

Comparing the theoretical and experimental results helped identify limitations in the initial model and evaluate improvements through parameter fitting.

---

[← Back to Portfolio](../)
