---
layout: default
title: Airplane Performance Analysis
---

# Airplane Performance Analysis

**The University of Alabama · AEM 368 · April 2026**

**Project Type:** Individual MATLAB programming project  
**Tools:** MATLAB  
**Methods:** Aerodynamic modeling, numerical analysis, and aircraft performance estimation  
**Status:** Completed

<p>
  <a href="/airplane-performance-program.pdf" target="_blank" rel="noopener noreferrer">
    View MATLAB Program and Results (PDF)
  </a>
</p>

## Project Overview

I organized the program into functions for atmospheric density, aerodynamic drag, propulsion performance, flight-speed limits, climb performance, sustained turns, and cruise calculations. Aircraft parameters are stored separately so the same analysis framework can evaluate both jet and propeller configurations.

The program evaluates altitude in 100 ft increments and uses interpolation to estimate flight-speed boundaries and ceiling altitudes. Range and endurance calculations account for decreasing aircraft weight as fuel is consumed.

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

The program generates simplified V–n diagrams at sea level, half the service ceiling, and the service ceiling. These diagrams combine stall boundaries with assumed load-factor limits of ±1.5 and the modeled maximum level-flight speed.

![Propeller aircraft V-n diagram](/airplane-prop-vn.png)

*Figure 4. Simplified propeller-aircraft V–n diagram at sea level using assumed ±1.5 load-factor limits.*

## Range and Endurance Analysis

The program estimates idealized cruise range and endurance using the specified drag polar, fuel-consumption parameters, and propulsion model. It numerically accounts for the reduction in aircraft weight as fuel is consumed.

Separate optimum lift coefficients are used for maximum range and maximum endurance for each propulsion type. These estimates exclude fuel reserves and fuel used during takeoff, climb, and descent.

The cruise integration does not enforce thrust or power feasibility at every weight step, so these results represent idealized estimates rather than verified mission capabilities.

## Calculated Performance Results

The MATLAB program produced the following summary results:

| Parameter | Jet Aircraft | Propeller Aircraft |
|---|---|---|
| Service Ceiling | 39,179 ft | 24,683 ft |
| Absolute Ceiling | 43,268 ft | 26,810 ft |
| Stall Equivalent Airspeed | 102.53 kt | 50.03 kt |
| Maximum True Airspeed | 580.22 kt | 154.94 kt |

The service-ceiling calculations use a maximum climb-rate threshold of 500 ft/min for the jet and 100 ft/min for the propeller aircraft. Absolute ceiling corresponds to zero maximum excess-power climb rate.

The maximum true airspeed is the highest modeled level-flight speed found across the evaluated altitudes up to the calculated absolute ceiling.

The results demonstrate differences between jet and propeller aircraft performance under the specified aerodynamic and propulsion assumptions.

## Model Assumptions and Limitations

The analysis uses a parabolic drag polar with fixed zero-lift drag coefficient, Oswald efficiency, and maximum lift coefficient. Atmospheric density varies with altitude, while available jet thrust and propeller power are assumed to scale with density ratio. Propeller efficiency and fuel-consumption parameters are held constant.

Compressibility effects, wave drag, and detailed engine operating limits are not modeled. In particular, the jet's predicted maximum speed of 580.22 kt should be interpreted as an output of this simplified model rather than a validated aircraft capability.

The results are theoretical predictions for the specified aircraft inputs and have not been validated against flight-test data.

## Engineering Takeaways

This project strengthened my understanding of aircraft performance, aerodynamic modeling, propulsion effects, and the relationships between airspeed, altitude, and flight capabilities.

Developing the MATLAB program provided experience with numerical calculations, data organization, engineering analysis, and technical visualization.

The project also demonstrated how a general computational framework can be used to evaluate different aircraft configurations and compare their operating characteristics.

---

[← Back to Portfolio](../)
