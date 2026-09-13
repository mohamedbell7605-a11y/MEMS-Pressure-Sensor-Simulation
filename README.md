\# MEMS Piezoresistive Pressure Sensor Simulation



\## Phase 1: Mechanical Simulation

\- \*\*Diaphragm Dimensions:\*\* 1000 µm × 1000 µm × 20 µm

\- \*\*Substrate Thickness:\*\* 400 µm

\- \*\*Boundary Conditions:\*\* Fixed substrate base, pressure load on diaphragm

\- \*\*Status:\*\* Validated structural mechanics and displacement response.



\## Phase 2: Electromechanical \& Piezoresistive Simulation



\### Key Performance Metrics

| Parameter | Symbol | Value | Unit |

| :--- | :--- | :--- | :--- |

| Baseline Resistance | $R\_0$ | 0.25066 | $\\Omega$ |++

| Full-Scale Resistance (100 kPa) | $R\_{\\text{max}}$ | 0.25083 | $\\Omega$ |

| Absolute Resistance Change | $\\Delta R$ | 0.00017 | $\\Omega$ |

| Fractional Resistance Change | $\\Delta R / R\_0$ | 0.0678 | % |

| Sensor Sensitivity | $S$ | $6.78 \\times 10^{-6}$ | $\\text{kPa}^{-1}$ |



\### Simulation Setup

\- \*\*Material:\*\* Single-crystal p-Silicon ($n\_d = 1 \\times 10^{16}\\ \\text{cm}^{-3}$)

\- \*\*Boundary Conditions:\*\* Terminal ($1\\text{ V}$), Ground ($0\\text{ V}$)

\- \*\*Parametric Sweep:\*\* $0$ to $100\\text{ kPa}$ (step: $20\\text{ kPa}$)

\- \*\*Response:\*\* Highly linear electromechanical output



# Phase 3: Wheatstone Bridge Integration & Voltage Sensitivity Analysis

## Overview
Integration of a full Wheatstone bridge circuit with the MEMS piezoresistive pressure sensor using COMSOL Multiphysics v6.1 (`Electrical Circuit` interface).

## Simulation Parameters & Results
- **Excitation Voltage ($V_{in}$):** 5.0 V
- **Pressure Range ($P_{app}$):** 0 to 100 kPa
- **Baseline Resistance ($R_0$):** 0.25066 Ω
- **Piezoresistive Sensitivity ($S$):** $6.78 \times 10^{-6}\text{ kPa}^{-1}$
- **Max Differential Output ($V_{out,max}$):** 3.39 mV
- **Total Bridge Sensitivity ($S_{bridge}$):** $0.00678\text{ mV/V/kPa}$ ($6.78\ \mu\text{V/V/kPa}$)

## Bridge Topology & Circuit Configuration
- **Full Wheatstone Bridge** connected via Nodes 0, 1, 2, 3
- **Tension Arms ($R_1, R_4$):** $R_0 (1 + S \cdot P_{app})$
- **Compression Arms ($R_2, R_3$):** $R_0 (1 - S \cdot P_{app})$
- **Differential Output Formula:** $V_{out} = V_3 - V_2$



# Phase 4: Thermal Drift & Sensitivity Analysis

## Overview
Evaluated ambient temperature variations (293.15 K to 353.15 K) on sensor baseline and piezoresistive sensitivity using full-bridge multiphysics modeling.

## Thermal Performance Metrics
- **Thermal Coefficient of Offset (TCO):** $0\ \mu\text{V/K}$ (Self-compensated full-bridge)
- **Thermal Coefficient of Sensitivity (TCS):** $-0.18\%/\text{K}$ ($-1800\text{ ppm/K}$)
- **$V_{out,max}$ at 293.15 K (20°C):** 3.39 mV
- **$V_{out,max}$ at 353.15 K (80°C):** 3.024 mV
- **Sensitivity Loss Over 60 K Span:** 10.8%