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

I developed a program in MATLAB to simulate a two-stage rocket launch from Kennedy Space Center and the orbital maneuvers needed to rendezvous with a target spacecraft in a polar geosynchronous orbit.

This program combines a numerical launch simulation with orbital calculations to model the mission from liftoff to rendezvous. This includes the following: launching the rocket, entering a transfer orbit, circularizing the orbit, coasting to the point where the orbital planes intersect, performing a plane change, and completing a two-impulse phasing maneuver to reach the target spacecraft.

Throughout the programming project, I worked on implementing the equations of motion (EOM), converting launch data into Earth-centered inertial coordinates, calculating orbital elements, and creating visualizations to better understand the spacecraft's trajectory and the timing of each maneuver.

## Launch and Deployment

The simulated mission starts with a simulated rocket launch from Kennedy Space Center in Merritt Island, Florida. I used MATLAB's ode45 solver to model the launch and solve the rocket's equations of motion (EOMs). I also used it to track how its position and velocity changed throughout the flight.

The simulation incorporated the following:

- Two-stage launch vehicle thrust and propellant characteristics.
- Gravitational acceleration and atmospheric drag.
- Gravity-turn and pitch-over maneuvers.
- Vehicle mass changes during propellant consumption.
- Earth-rotation correction when converting the deployment velocity to an inertial reference frame.

The simulation resulted in a deployment altitude of 218.11 km and an inertial speed of 6.249 km/s. I then used these values as the starting conditions for calculating the next part of the mission, the transfer-injection maneuver.

![Launch altitude versus time](/spacecraft-launch.png)

*Figure 1. Simulated launch altitude versus time.*

## Orbital Transfer and Plane Change

Using the simulated rocket's position and velocity at deployment, I was able to calculate the velocity change needed to enter an elliptical transfer orbit with an apogee radius of 42,164 km.

The modeled sequence includes the following:

1. Transfer-orbit injection at deployment.
2. Circularization at geosynchronous altitude.
3. A coast along the initial circular orbit to its intersection with the target orbital plane.
4. An impulsive plane change into the target polar plane.

I used the program to calculate the velocity changes needed for each maneuver, the time spent coasting between maneuvers, and the orbital elements throughout each phase of the mission.

![GTO transfer trajectory](/spacecraft-gto.png)

*Figure 2. Modeled elliptical transfer trajectory in the perifocal reference frame.*

## Spacecraft Rendezvous

I used the program to calculate a two-impulse phasing maneuver after completing the plane change to bring the chaser spacecraft into alignment with the target.

For this part of the mission, I accounted for how far the target spacecraft had traveled during the earlier maneuvers. I then calculated the orbital parameters, velocity changes, and timing needed for the chaser to reach the target's position afterwards.

![Spacecraft phasing orbit](/spacecraft-phasing.png)

*Figure 3. Simulated spacecraft phasing orbit in the final orbital plane.*

## Mission Results and Trajectory Visualization

The program calculates the orbital elements, velocity changes, and time required for each part of the mission. I also generated trajectory plots to visualize the spacecraft's path. Some of the main results from the simulation are shown in the table below.

| Parameter | Model Output |
|---|---:|
| Deployment altitude | 218.11 km |
| Deployment inertial speed | 6.249 km/s |
| Transfer-orbit semi-major axis | 24,380.05 km |
| Target circular-orbit radius | 42,164 km |
| Total post-deployment maneuver delta-v | 7,385.92 m/s |
| Total modeled mission duration, including launch | 33.76 hours |

I also created a 3D plot to show the spacecraft's path throughout the mission. It includes the elliptical transfer, initial geosynchronous coast, and phasing orbit. The plot also highlights where each maneuver takes place. This makes it easier to see how the spacecraft moves between the different orbits.

![3D spacecraft mission trajectory](/spacecraft-trajectory.png)

*Figure 4. Three-dimensional spacecraft trajectory from deployment through the modeled rendezvous sequence.*

## Model Assumptions and Limitations

This project uses a simplified mission model with the following assumptions:

- Spherical-Earth gravity and an exponential atmosphere.
- Constant drag coefficient and reference area, with no winds.
- Simplified launch equations that omit Coriolis acceleration.
- Instantaneous pitchover and stage separation.
- Impulsive orbital maneuvers and Keplerian coast segments.
- No optimization of the complete mission for minimum propellant consumption or total delta-v.

These results provide a good starting point for understanding how the mission would work in real life; however, the simulation is still a simplified model. To make it even more accurate, I would need to model the spacecraft's motion continuously, account for the time it would take to complete each engine burn, and check the final position and velocity of the chaser relative to the target to see how closely they match each other.

## Engineering Takeaways

This project helped me better understand orbital mechanics and how spacecraft trajectories can be modeled using MATLAB. By developing this MATLAB program, I gained hands-on aerospace engineering experience with numerical integration, coordinate transformations, calculating orbital elements, and planning orbital maneuvers. I also learned how to visualize spacecraft trajectories. This helped me better understand how the different stages of the mission connect.

---

[← Back to Portfolio](../)
