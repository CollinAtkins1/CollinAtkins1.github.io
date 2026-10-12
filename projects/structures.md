---
layout: default
title: Aerospace Structures Analysis
---

# Aerospace Structures Analysis

**The University of Alabama · AEM 341 · April 2026**

**Project Type:** Individual Course Project  
**Tools:** MATLAB  
**Methods:** Bernoulli–Euler Beam Theory, Unsymmetrical Bending, Experimental Comparison, Parameter Fitting

<p>
  <a href="/structures-part1.pdf" target="_blank" rel="noopener">
    View Part 1 — Analysis &amp; MATLAB Program (PDF)
  </a><br>
  <a href="/structures-part2.pdf" target="_blank" rel="noopener">
    View Part 2 — Experimental Comparison &amp; MATLAB Program (PDF)
  </a>
</p>

## Project Overview

I developed a MATLAB program to analyze bending of an unsymmetrical L-shaped cantilever beam. The model calculated cross-section properties, bending stresses, and deflections in both the horizontal and vertical directions.

In the second part of the project, I compared these predictions with strain and displacement measurements from the AEM 351 bidirectional bending lab. I then investigated how changing Young’s modulus and the assumed clamping conditions affected agreement with the measurements.

![L-shaped cantilever beam geometry](/beam-geometry.png)

*Figure 1. L-shaped cantilever beam, cross-section dimensions, and applied tip-load direction.*

## Part 1 — Computational Structural Analysis

I organized the MATLAB program into functions so that beam geometry, material properties, length, and tip loads could be changed without rewriting the main analysis.

The program calculated:

- Cross-sectional area and centroid location.
- Area moments of inertia and product of inertia.
- Bending moments and neutral-axis orientation.
- Bending stresses at ten specified strain-gage locations.
- Horizontal and vertical deflections along the beam.

For the selected case, I analyzed a 1 m aluminum beam under a downward 12 lbf tip load, using a Young’s modulus of 68.9 GPa and 1 mm spacing along the span.

The model predicted deflection in both directions even though the applied load was vertical. This coupled response results from the nonzero product of inertia of the L-shaped section in the chosen coordinate system.

![Horizontal and vertical deflections](/beam-deflections.png)

*Figure 2. Predicted horizontal and vertical deflections for the 12 lbf tip-load case with ideal clamping.*

## Part 2 — Experimental Comparison and Model Refinement

I extended the program to compare the beam model with experimental strain measurements at ten gages and displacement measurements at five locations along the span.

The baseline model used a Young’s modulus of 68.9 GPa and assumed zero displacement and slope at the clamped end. I evaluated three fitting approaches:

- Adjusting Young’s modulus while retaining ideal clamping.
- Fitting nonzero root displacements and slopes while retaining the nominal modulus.
- Fitting both the modulus and root boundary conditions together.

I compared the cases using the assigned percent-error measure and root-mean-square error (RMSE). This helped distinguish changes that improved displacement predictions from those that improved agreement with strain measurements.

![Theoretical and experimental comparison](/model-validation.png)

*Figure 3. Combined-fit model compared with experimental displacement, strain, and strain-derived stress for the 12 lbf load case.*

## Key Results

The displacement errors for each model are summarized below. RMSE measures the typical magnitude of the difference between predicted and measured displacement; smaller values indicate closer agreement.

| Model | Vertical displacement RMSE (mm) | Horizontal displacement RMSE (mm) |
|---|---:|---:|
| Baseline | 10.097 | 0.8518 |
| Fitted modulus only | 10.897 | 1.0425 |
| Fitted boundary conditions only | 1.1339 | 0.2117 |
| Combined fit | 0.8842 | 0.2256 |

Fitting the root boundary conditions produced a much larger improvement in displacement agreement than changing Young’s modulus alone. The combined fit reduced vertical displacement RMSE by approximately 91% relative to the baseline, while the boundary-only fit produced the lowest horizontal displacement RMSE.

The combined fit did not improve every response. It reduced side-gage strain error but increased base-gage strain error relative to the baseline, showing the tradeoffs involved in fitting several measurements at once.

## Model Assumptions and Limitations

The analysis uses linear-elastic Bernoulli–Euler beam theory and neglects shear deformation. The fitted root displacements and slopes represent departures from ideal clamping without explicitly modeling the clamp hardware.

The fitting results describe agreement with the selected 12 lbf dataset. Additional load cases or independent measurements would be needed to assess how well the fitted parameters predict other conditions. The fitted modulus should therefore be interpreted as an effective model parameter rather than a separate measurement of the material’s Young’s modulus.

## Engineering Takeaways

This project helped me connect beam theory with experimental measurements. I gained experience building modular MATLAB functions, analyzing coupled bending, fitting model parameters, and comparing predictions using quantitative error measures.

The most useful finding was that changing the support assumptions improved displacement agreement much more than adjusting Young’s modulus alone. It also showed me why a model should be evaluated against several measured responses rather than judged by a single error value.

---

[← Back to Portfolio](../)
