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

I developed a program in MATLAB to study how an unsymmetrical L-shaped cantilever beam bends under an applied load. Since the beam has an unsymmetrical cross-section, I calculated its following parameters: cross-sectional properties, bending stresses, and deflections in both the horizontal and vertical directions.

For the second part of the project, I compared the MATLAB results I obtained with the strain and displacement measurements I collected during the AEM 351 bidirectional bending lab. I also looked into how adjusting Young's modulus and changing the assumed clamping conditions affected how closely the model matched the experimental results.

![L-shaped cantilever beam geometry](/beam-geometry.png)

*Figure 1. L-shaped cantilever beam, cross-section dimensions, and applied tip-load direction.*

## Part 1 — Computational Structural Analysis

I organized my MATLAB code into separate functions to make it easier to adjust the beam's dimensions, material properties, length, and applied tip loads without having to rewrite the main program for each new case.

The program calculated the following parameters of the beam:

- Cross-sectional area and centroid location.
- Area moments of inertia and product of inertia.
- Bending moments and neutral-axis orientation.
- Bending stresses at ten specified strain-gage locations.
- Horizontal and vertical deflections along the beam.

For this specific part of the project, I modeled a 1 m long aluminum beam with a downward tip load of 12 lbf. I used a Young's modulus of 68.9 GPa and calculated the beam's deflection at 1 mm intervals along its entire length.

One interesting result I found was that the beam bent in both the horizontal and vertical directions, despite the load only being applied vertically. This happens because of the L-shaped cross-section. The L-shaped cross-section has a nonzero product of inertia in the coordinate system I used. As a result of the nonzero product of inertia, bending in one direction also causes deflection in the other.

![Horizontal and vertical deflections](/beam-deflections.png)

*Figure 2. Predicted horizontal and vertical deflections for the 12 lbf tip-load case with ideal clamping.*

## Part 2 — Experimental Comparison and Model Refinement

Next, I expanded my MATLAB program to compare the predicted behavior of the beam with the experimental data obtained from the lab. This included strain measurements from ten gages and displacement measurements taken at five different locations along the beam.

For the initial model, I used a Young's modulus of 68.9 GPa and assumed the clamped end was completely fixed, meaning it could not move or rotate. I evaluated the following three fitting approaches:

- Adjusting Young’s modulus while retaining ideal clamping.
- Fitting nonzero root displacements and slopes while retaining the nominal modulus.
- Fitting both the modulus and root boundary conditions together.

I compared the different cases using percent error and root-mean-square error (RMSE) to see how closely the theoretical model data matched the experimental data. This helped me figure out which changes made the displacement predictions more accurate and which ones gave me better results for the strain measurements.

![Theoretical and experimental comparison](/model-validation.png)

*Figure 3. Combined-fit model compared with experimental displacement, strain, and strain-derived stress for the 12 lbf load case.*

## Key Results

The displacement errors for all four model cases are summarized in the table below. I used RMSE to measure how far away the predicted displacements were from the actual measurements. Lower RMSE values mean the model's predictions are closer to the experimental results.

| Model | Vertical displacement RMSE (mm) | Horizontal displacement RMSE (mm) |
|---|---:|---:|
| Baseline | 10.097 | 0.8518 |
| Fitted modulus only | 10.897 | 1.0425 |
| Fitted boundary conditions only | 1.1339 | 0.2117 |
| Combined fit | 0.8842 | 0.2256 |

Adjusting the boundary conditions at the clamped end made a much bigger difference in how well the model matched the measured displacements than changing Young's modulus alone. When I adjusted both of them, the vertical displacement RMSE decreased by about 91% compared to the original model. However, I found that adjusting only the boundary conditions gave the best results for horizontal displacement.

I also found that adjusting both didn't improve every part of the model. While it helped reduce the strain error at the side gages, the error at the base gages actually increased compared to the base-gage strain error in the baseline model. This showed me that making the model more accurate in one area doesn't always mean it will give better results everywhere else in the model.

## Model Assumptions and Limitations

The theoretical model of the beam is based on linear-elastic Bernoulli–Euler beam theory, which basically assumes that shear deformation is small enough to ignore. I also allowed the clamped end to have some displacement and rotation to better match the experimental results, rather than just assuming it was perfectly fixed. However, I didn't model the actual clamp hardware for the beam.

The adjustments I made were based only on the measurements from the 12 lbf load case, and so I would need to test other loads or compare additional experimental data to see how well the model works under different conditions. The adjusted Young's modulus should be treated as a value that helps the model match the data because of this, rather than a direct measurement of the material's actual Young's modulus.

## Engineering Takeaways

This project helped me better understand how beam theory relates to actual experimental results. I gained hands-on experience in the following areas: writing MATLAB functions, studying bending in multiple directions, adjusting model parameters, and comparing predictions with lab measurements.

One of the biggest things I learned was how much the assumptions about the beam's support conditions can affect the final results. Changing these assumptions improved the displacement predictions much more than adjusting Young's modulus alone. I also learned that just because a model matches one set of measurements well doesn't mean it will accurately predict everything correctly. This is why it's important to compare several different results when evaluating a model instead of just relying on a single set.

---

[← Back to Portfolio](../)
