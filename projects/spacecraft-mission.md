
---
layout: default
title: Spacecraft Mission Design Program
---

# Spacecraft Mission Design Program

**The University of Alabama | AEM 369 | March 2026**

**Role:** Independent Project

**Tools:** MATLAB

**Methods:** Orbital Mechanics, Numerical Integration, Trajectory Simulation, Spacecraft Rendezvous

## Project Overview

I developed a MATLAB program to simulate a spacecraft mission involving launch, orbital insertion, transfer to geostationary orbital altitude, plane change, and spacecraft rendezvous.

The objective was to model a two-stage launch vehicle and determine the orbital maneuvers required for a chaser spacecraft to rendezvous with a target in a specified polar geosynchronous orbit.

The program calculates orbital parameters, required velocity changes, maneuver timing, and spacecraft trajectories.

## Launch and Orbital Insertion

The mission begins with a simulated launch from Kennedy Space Center in Florida.

I developed a numerical launch model using MATLAB's ode45 solver to integrate the vehicle's equations of motion.

The simulation incorporated:

- Two-stage launch vehicle thrust and propellant characteristics.
- Gravitational acceleration and atmospheric drag.
- Gravity-turn and pitch-over maneuvers.
- Vehicle mass changes during propellant consumption.
- Earth's rotation and inertial velocity calculations.

The simulated launch produced an orbital insertion altitude of approximately 218.11 km.

![Launch altitude versus time](/spacecraft-launch.png)

*Figure 1. Simulated launch altitude versus time.*

## Orbital Transfer and Plane Change

Following orbital insertion, the program calculates a Hohmann transfer to geostationary orbital altitude.

The orbital maneuver sequence includes:

1. Transfer from the insertion orbit to geostationary transfer orbit (GTO).
2. Circularization at geostationary orbital altitude.
3. Plane change into the target polar orbital plane.

The program calculates the velocity changes and orbital elements associated with these maneuvers.

![GTO transfer trajectory](/spacecraft-gto.png)

*Figure 2. Geostationary transfer orbit trajectory in the perifocal reference frame.*

## Spacecraft Rendezvous

After the plane change, the program calculates a two-impulse phasing maneuver to align the chaser spacecraft's position with the target.

The phasing analysis accounts for target motion during the preceding mission phases and determines the required orbital parameters, maneuver velocities, and timing.

![Spacecraft phasing orbit](/spacecraft-phasing.png)

*Figure 3. Simulated spacecraft phasing orbit in the final orbital plane.*

## Mission Results and Trajectory Visualization

The MATLAB program generated orbital parameters, velocity-change requirements, maneuver durations, and trajectory plots.

The simulation produced the following results:

| Parameter | Calculated Value |
|---|---|
| Orbital Insertion Altitude | 218.11 km |
| GTO Semi-Major Axis | 24,380.05 km |
| Target Orbital Semi-Major Axis | 42,164 km |
| Total Required Delta-V | 7,385.92 m/s |
| Total Mission Duration | 33.76 hours |

The program also generated a three-dimensional trajectory visualization showing the GTO transfer, initial GEO coast, phasing orbit, and maneuver locations.

![3D spacecraft mission trajectory](/spacecraft-trajectory.png)

*Figure 4. Three-dimensional spacecraft trajectory from deployment through the modeled rendezvous sequence.*

## Model Limitations

The mission analysis uses several simplifying assumptions, including:

- Simplified launch dynamics and atmospheric modeling.
- Instantaneous pitch-over and stage separation.
- Impulsive orbital maneuvers rather than finite-duration burns.
- Ideal Keplerian orbital motion between maneuvers.
- No optimization for minimum propellant consumption or total delta-v.

These assumptions make the program suitable for preliminary mission analysis rather than detailed mission verification.

## Engineering Takeaways

This project strengthened my understanding of spacecraft trajectory modeling, orbital mechanics, and numerical simulation.

Developing the MATLAB program provided experience with numerical integration, coordinate transformations, orbital elements, maneuver calculations, and trajectory visualization.

The project also demonstrated how individual mission phases can be integrated into a complete preliminary spacecraft mission analysis.

---

[← Back to Portfolio](../)
