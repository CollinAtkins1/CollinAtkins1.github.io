---
layout: default
title: Titan Sea Drone - Stability and Control
---

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

I am serving as the Stability and Control Lead for my senior aerospace engineering design project at The University of Alabama.

Our team is developing a VTOL drone concept designed to fly through Titan's atmosphere, land on its hydrocarbon seas, and collect liquid samples for scientific analysis.

The mission concept includes battery-powered flight, radioisotope thermoelectric generator (RTG) trickle charging, and a preliminary flight-range requirement of at least 10 kilometers per battery charge.

My responsibilities involve developing the vehicle's flight-dynamics and control-system approach to support stable and controlled operation throughout the mission.

## My Contributions to Date

As Stability and Control Lead, I developed the subsystem design plan and identified the information needed from the structures, propulsion, aerodynamics, and electronics teams.

My completed work includes:

- A preliminary qualitative comparison of PID and LQR control.
- A proposed PID baseline for initial hover-control development.
- Identification of required model inputs, including mass properties, rotor geometry, thrust characteristics, and actuator response.
- A preliminary risk assessment and staged verification plan.
- Fall and spring schedules aligned with the team's design milestones.

The next step is to use the team's preliminary vehicle parameters to develop the hover model and evaluate control margins.

## Stability and Control Design

I am developing a parameterized flight-dynamics modeling approach using MATLAB, with Simulink planned for controller development and evaluation.

The model will incorporate:

- Vehicle mass and moments of inertia.
- Center-of-gravity location.
- Rotor arrangement and spin directions.
- Rotor thrust and reaction torque characteristics.
- Motor response and actuator limitations.
- Atmospheric and operating conditions on Titan.

The initial analysis will focus on hover before expanding to forward flight, descent, and sea-landing operations.

The proposed methods include rigid-body equations of motion, linearized state-space modeling, eigenvalue analysis, and controllability analysis.

## Controller Trade Study — PID vs. LQR

I conducted a preliminary qualitative trade study comparing proportional-integral-derivative (PID) control and linear-quadratic regulation (LQR) as candidate feedback control approaches.

| Criterion | PID | LQR |
|---|---|---|
| Development | Incremental feedback-loop tuning | State-feedback gain design |
| Coupled Motion | Evaluate interactions between loops | Represent coupling in a state-space model |
| Motor Limits | Saturation and anti-windup considerations | Saturation and control-effort considerations |

PID was proposed as the initial baseline for hover-control development because its feedback loops can be tuned incrementally.

LQR remains an alternative for future evaluation.

The planned quantitative comparison will evaluate tracking accuracy, response time, overshoot, control effort, and sensitivity to vehicle parameter changes.

## Control Authority and Design Considerations

The stability and control design must account for the vehicle's mass properties, rotor arrangement, actuator limits, and operating conditions.

Key design considerations include:

- Control of altitude, roll, pitch, and yaw.
- Allowable center-of-gravity range.
- Available thrust and control moments.
- Rotor and motor saturation limits.
- Descent-rate and attitude constraints during sea landing.
- Integration with propulsion, structures, and electronics subsystems.

The preliminary analysis will help guide vehicle configuration decisions as subsystem parameters become available.

## Risk Management and Verification

I developed a preliminary risk-management and verification approach addressing uncertain mass properties, insufficient control authority, actuator saturation, and integration challenges.

![Stability and Control Risk Assessment Matrix](/risk-matrix.png)

*Figure 1. Preliminary stability and control risk assessment, including likelihood, impact, and proposed mitigation strategies.*

The planned verification process includes:

1. MATLAB flight-dynamics modeling.
2. Simulink controller development and simulation.
3. Motor and rotor characterization.
4. Sensor calibration and subsystem integration.
5. Restrained and low-altitude hover testing.
6. Flight testing of an Earth-based demonstrator.

Separate Earth and Titan operating parameters will be maintained because Earth-based testing cannot directly validate performance under Titan's atmospheric conditions.

## Project Timeline and Milestones

The stability and control development schedule is organized into fall and spring phases and aligned with the senior design team's major project milestones.

### Fall 2026 — Preliminary Design

The fall semester focuses on establishing stability and control requirements, developing preliminary flight-dynamics models, evaluating controller approaches, and preparing the verification plan.

![Fall Stability and Control Gantt Chart](/fall-gantt.png)

*Figure 2. Fall 2026 stability and control project timeline and milestones.*

### Spring 2027 — Development and Testing

The spring semester is planned to focus on refining the flight-dynamics and control models, integrating the major subsystems, and conducting staged ground and flight testing.

![Spring Stability and Control Gantt Chart](/spring-gantt.png)

*Figure 3. Spring 2027 stability and control development and testing schedule.*

## Next Steps

The next stage will focus on developing the parameterized hover model and establishing preliminary control margins. Required inputs include vehicle mass, moments of inertia, rotor locations, thrust limits, and motor response.

I will then compare PID and LQR under the same simulated conditions using tracking error, settling time, overshoot, control effort, and sensitivity to parameter changes. The analysis will also check actuator saturation and the effects of center-of-gravity shifts.

Future updates will include model assumptions, controller response plots, and comparisons with Earth-demonstrator test data as they become available.

I plan to update this page with MATLAB and Simulink results, controller response plots, and additional engineering findings as the design progresses.

---

[← Back to Portfolio](../)
