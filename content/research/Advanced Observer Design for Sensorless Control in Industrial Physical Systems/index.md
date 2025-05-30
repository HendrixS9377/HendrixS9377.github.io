---
title: Advanced Observer Design for Sensorless Control in Industrial Physical Systems
summary: Proposed an improved high-order sliding mode observer (HOSM) with hyperbolic tangent function for sensorless PMSM control, demonstrating high estimation accuracy and robustness across speed conditions and parametric uncertainties.
date: 2024-04-29
type: docs
tags:
  - Control
  - PMSM
  - Cyber-Physical Systems
image:
  caption: 'Improved HOSM observer architecture for PMSM drives'
---

This work addresses the challenge of **sensorless control** in industrial **permanent magnet synchronous motor (PMSM)** drives by proposing a novel **improved high-order sliding mode observer (HOSM)**. The observer enhances estimation performance of rotor speed and position, eliminating the need for mechanical sensors, which are often unreliable in harsh industrial environments.

## Research Objectives

- Develop a **robust observer** for estimating PMSM speed and position using only voltage and current measurements.
- Minimize **chattering effects** typical in classical sliding mode observers.
- Ensure **finite-time stability** and robustness against **parametric uncertainties** such as resistance/inductance mismatch.

## Core Contributions

### 1. Improved HOSM Observer Design
The proposed observer leverages a **modified super-twisting algorithm** with the following key enhancements:
- Replacement of the signum function with a **hyperbolic tangent function** to reduce chattering.
- Integration of **linear and integral terms** to enhance convergence and robustness.
- Formal proof of **finite-time stability** using **Lyapunov analysis**.

Mathematically, back-EMF \( \hat{e}_j \) is estimated via:
\[
\hat{e}_j = K_2 \int_0^t \phi_2(s_j(\tau)) \, d\tau
\]

### 2. PMSM System Modeling and Control
- A complete field-oriented control (FOC) architecture is implemented using double-PI current control and SVPWM.
- Speed estimation is used as feedback to enable full **sensorless closed-loop control**.

### 3. Simulation Studies
The proposed observer is evaluated under:
- **Constant speed** (500 rpm)
- **Variable speed profiles** (1000–1500 rpm)
- **Parameter uncertainties** (±10% in R and Ls)
- **Gain perturbations** (±25% sinusoidal variation)

Results show:
- **<0.5 mA** current estimation error under steady conditions.
- **<1% speed estimation error** under uncertainty scenarios.
- Significant improvement over classical SMO and baseline HOSM designs.

## Conclusion

This study presents a high-precision, robust observer for **sensorless PMSM control**. The proposed improved HOSM:
- Eliminates the need for low-pass filtering,
- Enables faster convergence,
- Maintains accuracy under uncertain parameters and speed transients.

This design offers a reliable solution for **industrial cyber-physical systems (CPSs)** where precision and resilience are critical.

📄 [IEEE ICPS 2024 Conference Paper] — Presented
