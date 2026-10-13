---
layout: default
title: Titan Sea Drone - Stability and Control
---
# Titan Sea Drone — Stability and Control

**Senior Design Project · The University of Alabama · August 2026–Present**

**Role:** Stability and Control Lead  
**Status:** Preliminary design; modeling and verification planning  
**Planned Analysis Tools:** MATLAB and Simulink

<p>
  <a href="/titan-design-plan.pdf" target="_blank" rel="noopener noreferrer">
    View Stability and Control Design Plan (PDF)
  </a>
</p>

<p>
  <a href="/titan-controller-trade-study.pdf" target="_blank" rel="noopener noreferrer">
    View Controller Trade Study (PDF)
  </a>
</p>

## Project Overview

I am currently serving as the Stability and Control Lead for my senior aerospace engineering design project at The University of Alabama.

For our senior design project, my team is designing a VTOL drone that can fly through Titan's dense atmosphere, land on its hydrocarbon seas, and collect liquid samples for scientific research via a vacuum mechanism.

Our design uses battery-powered flight, with a radioisotope thermoelectric generator (RTG) to slowly recharge the batteries between flights during nighttime. One of our initial design goals is for the drone to be able to travel at least 10 kilometers on a single battery charge before landing on a hydrocarbon sea.

My main responsibility in this project is to focus on the drone's stability and control development. This includes developing an approach to its flight dynamics and control systems to help make sure the vehicle can fly, maneuver, and operate safely throughout the mission.

## My Contributions to Date

As the Stability and Control Lead, I put together a plan for developing our subsystem and worked out what information I would need from the other subsystem leads, such as structures, propulsion, aerodynamics, and electronics, to move forward with our overall design.

My completed work so far includes the following:

- A preliminary qualitative comparison of PID and LQR control.
- A proposed PID baseline for initial hover-control development.
- Identification of required model inputs, including mass properties, rotor geometry, thrust characteristics, and actuator response.
- A preliminary risk assessment and staged verification plan.
- Fall and spring schedules aligned with the team's design milestones.

My next step is to use the preliminary vehicle specifications from the team to build a hover model in MATLAB and determine how much control authority the drone will have to maintain stable flight.

## Stability and Control Design

I am working on the development of a flight-dynamics model in MATLAB that will allow me to adjust the drone's design parameters as our team continues developing the vehicle. I also plan to use Simulink to develop and test the control system as the team progresses.

The model will incorporate the following flight parameters:

- Vehicle mass and moments of inertia.
- Center-of-gravity location.
- Rotor arrangement and spin directions.
- Rotor thrust and reaction torque characteristics.
- Motor response and actuator limitations.
- Atmospheric and operating conditions on Titan.

I plan to start by modeling how the drone behaves while hovering. Afterwards, I will expand the analysis to include forward flight, descent, and landing on Titan's seas.

To do this, I will use rigid-body equations of motion to model the drone's movement. I will also use linearized state-space models to study its stability. I plan to use eigenvalue and controllability analyses to better understand how the drone responds to disturbances and how effectively it can be controlled as well.

## Controller Trade Study — PID vs. LQR

I also conducted a qualitative trade study on two possible control methods: proportional-integral-derivative (PID) control and linear-quadratic regulation (LQR). This was done to better understand their advantages and disadvantages before making a final decision on which approach would work best for our drone.

| Criterion | PID | LQR |
|---|---|---|
| Development | Incremental feedback-loop tuning | State-feedback gain design |
| Coupled Motion | Evaluate interactions between loops | Represent coupling in a state-space model |
| Motor Limits | Saturation and anti-windup considerations | Check actuator saturation; control-effort penalties do not enforce hard limits |

I proposed starting with PID control for the hover model, primarily because it allows me to adjust and tune the feedback loops one at a time. I plan to keep LQR as an alternative option to explore as the design progresses.

Once both of the control models are developed, I plan to compare them using the results from the following tests: how accurately they follow commands, how quickly they respond, how much they overshoot, and how much control effort they require. I also want to see how well each method performs when the drone's design parameters change.

## Control Authority and Design Considerations

I will also need to consider the drone's mass and weight distribution, how its rotors are arranged, the limits of its motors and other actuators, and the conditions it will experience during the mission when developing the stability and control system.

Key design considerations include the following parameters:

- Control of altitude, roll, pitch, and yaw.
- Allowable center-of-gravity range.
- Available thrust and control moments.
- Rotor and motor saturation limits.
- Descent-rate and attitude constraints during sea landing.
- Integration with propulsion, structures, and electronics subsystems.

As the other subsystem leads obtain and provide more information concerning their subsystems, I will use the initial analysis to help me make decisions about the stability and control design and configuration for the drone.

## Risk Management and Verification

I also put together an initial plan to identify any potential risks and check that the control system meets its design requirements. Some of the main concerns I considered were uncertainties in the drone's mass and weight distribution, whether it would have enough control authority to maintain stable flight, the limits of its actuators, and possible challenges when combining the different subsystems.

![Stability and Control Risk Assessment Matrix](/risk-matrix.png)

*Figure 1. Preliminary stability and control risk assessment, including likelihood, impact, and proposed mitigation strategies.*

The planned verification process includes the following listed steps:

1. MATLAB flight-dynamics modeling.
2. Simulink controller development and simulation.
3. Motor and rotor characterization.
4. Sensor calibration and subsystem integration.
5. Restrained and low-altitude hover testing.
6. Flight testing of an Earth-based demonstrator.

I plan to maintain separate sets of operating parameters for Earth and Titan. Earth-based testing will help evaluate the control-system implementation; however, it cannot directly validate performance under Titan’s operating conditions.

## Project Timeline and Milestones

I organized the stability and control development schedule around the fall and spring semesters into a pair of Gantt charts, making sure my planned work lines up with the major deadlines and milestones of the team at the same time.

### Fall 2026 — Preliminary Design

I am mainly focused on defining the stability and control requirements, building the initial flight-dynamics models, comparing possible control methods, and putting together a plan to test and verify the system's performance during the fall semester.

![Fall Stability and Control Gantt Chart](/fall-gantt.png)

*Figure 2. Fall 2026 stability and control project timeline and milestones.*

### Spring 2027 — Development and Testing

Later on, I plan to improve the flight-dynamics and control models as our design becomes more developed during the spring semester. I will also work with the other teams to integrate the major subsystems and help carry out ground and flight tests in stages to evaluate the drone's stability and control performance.

![Spring Stability and Control Gantt Chart](/spring-gantt.png)

*Figure 3. Spring 2027 stability and control development and testing schedule.*

## Next Steps

My next step in stability and control development is to develop a hover model that I can update as the team's design becomes more mature and detailed. To do this, I will need information such as the following parameters of the drone: mass, moments of inertia, rotor positions, thrust limits, and motor response. I will then use this model to get an initial idea of how much control authority the drone has during hover.

I plan to test PID and LQR controllers under the same simulated conditions to see how they compare once the model is ready. I will be looking at how accurately each controller follows commands, how quickly the drone settles, how much it overshoots, and how much control effort is needed. I also want to see how changes in the drone's parameters, shifts in its center of gravity, and actuator limits affect its stability and performance.

As the project moves forward, I plan to constantly update this page with the most up-to-date MATLAB and Simulink results, controller response plots, and explanations of the assumptions used in my models. I will also compare the simulations with data from our Earth-based test vehicle as those results become available. This will help show how the design develops and what I've learned throughout the project as it progresses.

---

[← Back to Portfolio](../)
