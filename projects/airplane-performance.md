
---
layout: default
title: Airplane Performance Analysis
---

# Airplane Performance Analysis

**The University of Alabama | AEM 368 | April 2026**

**Project Type:** Individual MATLAB Programming Project

**Tools:** MATLAB

**Methods:** Aircraft Performance Analysis, Aerodynamics, Numerical Methods, Flight Mechanics

## Project Overview

I developed a MATLAB program to evaluate and compare the flight performance of jet-powered and propeller-driven airplanes.

The objective was to calculate aircraft performance characteristics across varying airspeeds and altitudes using aerodynamic, propulsion, and atmospheric models.

The program evaluates thrust, drag, power, climb performance, maneuvering capabilities, range, endurance, and operational flight limits for both aircraft configurations.

## MATLAB Program Development

I organized the program using functions to perform calculations for both jet and propeller aircraft using their respective geometric, aerodynamic, and propulsion parameters.

The analysis incorporates:

- Aircraft weight, wingspan, wing area, and aerodynamic coefficients.
- Atmospheric density variations with altitude.
- Parasite and induced drag.
- Thrust and power available and required.
- Stall speed and operational airspeed limits.
- Maximum rate of climb and sustained turn rate.
- Service and absolute ceilings.
- Maximum range and endurance.

The program performs calculations across a range of altitudes and airspeeds and generates plots to visualize the results.

## Thrust, Drag, and Power Analysis

The MATLAB program calculates thrust and power requirements for steady, level flight using aerodynamic drag relationships.

For the jet aircraft, the analysis compares available thrust against required drag to determine feasible flight speeds at different altitudes.

![Jet aircraft thrust and drag analysis](/airplane-jet-thrust.png)

*Figure 1. Jet aircraft thrust and drag versus equivalent airspeed at selected altitudes.*

For the propeller aircraft, the analysis evaluates power required and available across the flight-speed range.

![Propeller aircraft power analysis](/airplane-prop-power.png)

*Figure 2. Propeller aircraft power required and available versus equivalent airspeed.*

## Climb Performance and Maneuverability

I calculated maximum rate of climb as a function of altitude using the excess power available for each aircraft configuration.

The results demonstrate how increasing altitude influences the available climb performance.

![Jet aircraft rate of climb](/airplane-jet-climb.png)

*Figure 3. Calculated maximum rate of climb versus altitude for the jet aircraft.*

The program also generates V-n diagrams to illustrate maneuvering load-factor limits at sea level, half the service ceiling, and the service ceiling.

![Propeller aircraft V-n diagram](/airplane-prop-vn.png)

*Figure 4. Calculated propeller aircraft V-n envelope at sea level.*

## Range and Endurance Analysis

The program calculates maximum range and endurance for both aircraft configurations using aerodynamic efficiency, propulsion characteristics, and fuel-consumption models.

The analysis accounts for changes in aircraft weight as fuel is consumed and evaluates how altitude affects the predicted performance.

## Calculated Performance Results

The MATLAB program produced the following summary results:

| Parameter | Jet Aircraft | Propeller Aircraft |
|---|---|---|
| Service Ceiling | 39,179 ft | 24,683 ft |
| Absolute Ceiling | 43,268 ft | 26,810 ft |
| Stall Equivalent Airspeed | 102.53 kt | 50.03 kt |
| Maximum True Airspeed | 580.22 kt | 154.94 kt |

The results demonstrate differences between jet and propeller aircraft performance under the specified aerodynamic and propulsion assumptions.

## Model Assumptions and Limitations

The analysis uses simplified aerodynamic and propulsion models, including fixed aerodynamic coefficients and modeled changes in thrust or power availability with altitude.

The calculated flight-performance characteristics represent theoretical predictions for the specified aircraft parameters rather than experimentally validated performance.

## Engineering Takeaways

This project strengthened my understanding of aircraft performance, aerodynamic modeling, propulsion effects, and the relationships between airspeed, altitude, and flight capabilities.

Developing the MATLAB program provided experience with numerical calculations, data organization, engineering analysis, and technical visualization.

The project also demonstrated how a general computational framework can be used to evaluate different aircraft configurations and compare their operating characteristics.

---

[← Back to Portfolio](../)
