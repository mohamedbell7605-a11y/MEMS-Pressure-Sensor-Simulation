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

| Baseline Resistance | $R\_0$ | 0.25066 | $\\Omega$ |

| Full-Scale Resistance (100 kPa) | $R\_{\\text{max}}$ | 0.25083 | $\\Omega$ |

| Absolute Resistance Change | $\\Delta R$ | 0.00017 | $\\Omega$ |

| Fractional Resistance Change | $\\Delta R / R\_0$ | 0.0678 | % |

| Sensor Sensitivity | $S$ | $6.78 \\times 10^{-6}$ | $\\text{kPa}^{-1}$ |



\### Simulation Setup

\- \*\*Material:\*\* Single-crystal p-Silicon ($n\_d = 1 \\times 10^{16}\\ \\text{cm}^{-3}$)

\- \*\*Boundary Conditions:\*\* Terminal ($1\\text{ V}$), Ground ($0\\text{ V}$)

\- \*\*Parametric Sweep:\*\* $0$ to $100\\text{ kPa}$ (step: $20\\text{ kPa}$)

\- \*\*Response:\*\* Highly linear electromechanical output

