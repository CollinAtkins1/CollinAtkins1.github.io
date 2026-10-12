---
layout: default
title: Titan Sea Drone - Stability and Control
---

# Titan Sea Drone — Stability and Control

**Senior Design Project | The University of Alabama | August 2026 – Present**

**Role:** Stability and Control Lead

**Tools:** MATLAB, Simulink

**Status:** Preliminary Design and Development

## Project Overview

I am serving as the Stability and Control Lead for my senior aerospace engineering design project at The University of Alabama.

Our team is developing a VTOL drone concept designed to fly through Titan's atmosphere, land on its hydrocarbon seas, and collect liquid samples for scientific analysis.

The mission concept includes battery-powered flight, radioisotope thermoelectric generator (RTG) trickle charging, and a preliminary flight-range requirement of at least 10 kilometers per battery charge.

My responsibilities involve developing the vehicle's flight-dynamics and control-system approach to support stable and controlled operation throughout the mission.

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

The planned verification process includes:

1. MATLAB flight-dynamics modeling.
2. Simulink controller development and simulation.
3. Motor and rotor characterization.
4. Sensor calibration and subsystem integration.
5. Restrained and low-altitude hover testing.
6. Flight testing of an Earth-based demonstrator.

Separate Earth and Titan operating parameters will be maintained because Earth-based testing cannot directly validate performance under Titan's atmospheric conditions.

## Current Progress and Next Steps

The project is in the preliminary design phase.

My current focus includes controller selection, identifying required subsystem parameters, developing the flight-dynamics modeling approach, and establishing verification criteria.

Future work will involve controller implementation, evaluating stability and control margins, integrating subsystem models, and comparing predicted performance against testing results.

I plan to update this page with MATLAB and Simulink results, controller response plots, and additional engineering findings as the design progresses.

---

[← Back to Portfolio](../)

---

[← Back to Portfolio](../)
