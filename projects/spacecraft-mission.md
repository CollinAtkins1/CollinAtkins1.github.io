---
layout: default
title: Spacecraft Mission Design Program
---

# Spacecraft Mission Design Program

**The University of Alabama · AEM 369 · March 2026**

**Project Type:** Individual Course Project  
**Tools:** MATLAB  
**Methods:** Numerical Integration, Launch Dynamics, Orbital Mechanics, Coordinate Transformations, Impulsive Maneuver Analysis

<a href="/spacecraft-mission.pdf" target="_blank" rel="noopener">
  View MATLAB Program &amp; Results (PDF)
</a>

## Project Overview

## Project Overview

I developed a MATLAB program to model a two-stage launch from Kennedy Space Center and a sequence of orbital maneuvers for rendezvous with a target spacecraft in a polar geosynchronous orbit.

The program combines numerical launch simulation with analytical orbital calculations to estimate transfer trajectories, velocity-change requirements, and mission timing. The modeled sequence includes launch, transfer-orbit injection, circularization, a coast to the intersection of the orbital planes, a plane change, and a two-impulse phasing maneuver.

My work included implementing the equations of motion, converting launch states into Earth-centered inertial coordinates, calculating orbital elements, and generating trajectory visualizations.

## Launch and Deployment

The mission begins with a simulated launch from Kennedy Space Center in Florida.

I developed a numerical launch model using MATLAB's ode45 solver to integrate the vehicle's equations of motion.

The simulation incorporated:

- Two-stage launch vehicle thrust and propellant characteristics.
- Gravitational acceleration and atmospheric drag.
- Gravity-turn and pitch-over maneuvers.
- Vehicle mass changes during propellant consumption.
- Earth-rotation correction when converting the deployment velocity to an inertial reference frame.

The modeled launch reached a deployment altitude of 218.11 km and an inertial speed of 6.249 km/s. This deployment state provided the initial conditions for the transfer-injection maneuver.

![Launch altitude versus time](/spacecraft-launch.png)

*Figure 1. Simulated launch altitude versus time.*

## Orbital Transfer and Plane Change

Starting from the deployment state, the program calculates an impulsive injection into an elliptical transfer orbit with an apogee radius of 42,164 km.

The modeled sequence includes:

1. Transfer-orbit injection at deployment.
2. Circularization at geosynchronous altitude.
3. A coast along the initial circular orbit to its intersection with the target orbital plane.
4. An impulsive plane change into the target polar plane.

The program calculates the velocity changes, coast times, and orbital elements associated with these phases.

![GTO transfer trajectory](/spacecraft-gto.png)

*Figure 2. Modeled elliptical transfer trajectory in the perifocal reference frame.*

## Spacecraft Rendezvous

After the plane change, the program calculates a two-impulse phasing maneuver to align the chaser spacecraft's position with the target.

The phasing analysis accounts for target motion during the preceding mission phases and determines the required orbital parameters, maneuver velocities, and timing.

![Spacecraft phasing orbit](/spacecraft-phasing.png)

*Figure 3. Simulated spacecraft phasing orbit in the final orbital plane.*

## Mission Results and Trajectory Visualization

The program reports orbital elements, impulsive velocity changes, elapsed times, and trajectory plots. Selected outputs from the modeled mission are summarized below.

| Parameter | Model Output |
|---|---:|
| Deployment altitude | 218.11 km |
| Deployment inertial speed | 6.249 km/s |
| Transfer-orbit semi-major axis | 24,380.05 km |
| Target circular-orbit radius | 42,164 km |
| Total post-deployment maneuver delta-v | 7,385.92 m/s |
| Total modeled mission duration, including launch | 33.76 hours |

The program also generated a three-dimensional trajectory visualization showing the GTO transfer, initial GEO coast, phasing orbit, and maneuver locations.

![3D spacecraft mission trajectory](/spacecraft-trajectory.png)

*Figure 4. Three-dimensional spacecraft trajectory from deployment through the modeled rendezvous sequence.*

## Model Assumptions and Limitations

This project uses a simplified mission model with:

- Spherical-Earth gravity and an exponential atmosphere.
- Constant drag coefficient and reference area, with no winds.
- Simplified launch equations that omit Coriolis acceleration.
- Instantaneous pitchover and stage separation.
- Impulsive orbital maneuvers and Keplerian coast segments.
- No optimization of the complete mission for minimum propellant consumption or total delta-v.

The results represent an educational mission-analysis case. Further verification would require continuous trajectory propagation, finite-duration burn modeling, and checks of the final relative position and velocity between the chaser and target.

## Engineering Takeaways

This project strengthened my understanding of spacecraft trajectory modeling, orbital mechanics, and numerical simulation.

Developing the MATLAB program provided experience with numerical integration, coordinate transformations, orbital elements, maneuver calculations, and trajectory visualization.

The project also demonstrated how individual mission phases can be integrated into a complete preliminary spacecraft mission analysis.

---

[← Back to Portfolio](../)
