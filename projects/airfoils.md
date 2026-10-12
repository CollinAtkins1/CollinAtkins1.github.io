# NACA Airfoil Analysis

The University of Alabama · AEM 313 · April 2026

**Role:** Aerodynamics Analyst / Project Co-Lead

**Tools:** XFOIL, Microsoft Excel

**Methods:** Thin Airfoil Theory, Inviscid and Viscous Aerodynamic Analysis

<a href="airfoil-report.pdf" target="_blank" rel="noopener">
  View Project Report (PDF)
</a>

## Project Overview

This group project investigated the aerodynamic performance of six NACA 4-digit airfoils using Thin Airfoil Theory (TAT) and XFOIL.

The objective was to evaluate how changes in the maximum camber, camber location, thickness, and Reynolds number affect its lift characteristics, pitching moments, pressure distributions, and overall aerodynamic performance.

The six airfoils analyzed were NACA 1108, 2408, 1408, 2308, 4408, and 0008.

My individual contributions focused on NACA 2408, NACA 1408, and NACA 2308. This included the theoretical calculations, XFOIL simulations, aerodynamic plots, and technical documentation of these three airfoils.

## Thin Airfoil Theory Analysis

Thin Airfoil Theory was used to calculate aerodynamic characteristics based on airfoil camber geometry.

The analysis included the following:

- Mean camber-line calculations.
- Zero-lift angle of attack.
- Pitching-moment coefficients.
- Center-of-pressure location.
- Theoretical lift coefficients.

The analytical results obtained from the TAT analysis provided a baseline for comparison with XFOIL simulations.

## XFOIL Aerodynamic Analysis

<p>I also conducted inviscid and viscous XFOIL analyses of NACA 2408, 1408, and 2308, using a baseline Reynolds number of Re = 10<sup>6</sup> for the viscous comparisons.</p>

Lift coefficients were compared to each other over varying angles of attack, and the results were plotted in Excel alongside TAT predictions.

The project included comparisons of the following:

- Theoretical and numerical lift curves.
- Inviscid and viscous flow predictions.
- Pressure-coefficient distributions.
- The influence of airfoil camber and camber location.
- The effect of airfoil thickness on aerodynamic performance.

## Key Results and Findings

### Camber Effects

The analysis showed that increasing airfoil camber would generally increase lift at a given angle of attack and shift the zero-lift angle in the negative direction.

For example, the theoretical zero-lift angles were the following:

| Airfoil | Zero-Lift Angle |
|---|---|
| NACA 1408 | -1.0386° |
| NACA 2408 | -2.0772° |
| NACA 2308 | -1.9180° |

These results demonstrate the influence of camber magnitude and location on aerodynamic characteristics.

![NACA airfoil mean camber lines](/airfoil-camber.png)

*Figure 1. Mean camber lines for the six NACA airfoils.*

### Lift-Curve Comparisons

TAT and XFOIL both produced similar lift predictions within the approximately linear operating region.

Differences between theoretical and numerical predictions became more apparent when viscous effects and higher angles of attack were added to consideration.

![NACA 2408 lift-curve comparison](/airfoil-lift.png)

*Figure 2. Thin Airfoil Theory and XFOIL lift-curve comparison for NACA 2408.*

### Thickness Variation

Additional simulations investigated the influence of thickness on the NACA 24xx airfoil family.

The results obtained were used to compare changes in lift behavior and the effects of thickness under inviscid and viscous conditions.

![NACA 2408 thickness variation](/airfoil-thickness.png)

Figure 3. Effect of thickness variation on the viscous lift curves of the NACA 24xx airfoil family.

### Pressure-Coefficient Distributions

Pressure-coefficient distributions were generated using XFOIL to compare the inviscid and viscous predictions at different angles of attack.

These plots showed how pressure varies along the airfoil chord and allowed comparison of inviscid and viscous predictions. The NACA 2408 example at 4° shows close agreement between the two solutions, with small differences due to viscous effects.

![NACA 2408 pressure-coefficient comparison](/airfoil-cp.png)

<p><em>Figure 4. Inviscid and viscous pressure-coefficient distributions for NACA 2408 at α = 4°, with Re = 10<sup>6</sup> for the viscous solution.</em></p>

## Engineering Takeaways

This project strengthened my understanding of aerodynamic modeling, airfoil geometry, and the limitations of simplified analytical methods and my technical skills using XFOIL and Excel.

Comparing my TAT results with my XFOIL results helped demonstrate the importance of numerical simulation when evaluating aerodynamic characteristics under different flow conditions.

The project also provided me experience in processing simulation data, interpreting aerodynamic plots, and communicating my technical findings in an engineering report.

## Project Contributions

This was a two-person group project completed with a fellow aerospace engineering classmate in AEM313. 

My individual responsibilities included the NACA 2408, 1408, and 2308 analyses, aerodynamic calculations, XFOIL simulations, Excel plots, and contributions to the report's methodology, results, and formatting.

---

[← Back to Portfolio](../)
