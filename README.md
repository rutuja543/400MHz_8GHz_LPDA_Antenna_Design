# 400 MHz–8 GHz Log-Periodic Dipole Array (LPDA)

## Overview

This project presents the design, simulation, and analysis of a **wideband Log-Periodic Dipole Array (LPDA)** antenna covering the frequency range from **400 MHz to 8 GHz**.

The antenna was designed and simulated using **4NEC2 (NEC2 Method of Moments)**. The design focuses on studying the behavior of a multi-element log-periodic structure across a very wide frequency range, including input impedance, SWR, radiation pattern, gain, and directional behavior.

The project was developed as part of the **METIX RF Students Antenna Design Contest 2026**.

---

## Project Objectives

- Design an LPDA antenna covering **400 MHz–8 GHz**.
- Develop the antenna geometry using log-periodic scaling.
- Simulate the antenna using **4NEC2**.
- Analyze input impedance and SWR across the operating band.
- Study radiation patterns at different frequencies.
- Analyze antenna gain and directional behavior.
- Understand the effect of LPDA parameters on broadband performance.

---

## Antenna Specifications

| Parameter | Value |
|---|---:|
| Antenna Type | Log-Periodic Dipole Array (LPDA) |
| Frequency Range | 400 MHz – 8 GHz |
| Number of Elements | 35 |
| Scaling Factor (τ) | 0.90 |
| Spacing Factor (σ) | 0.16 |
| Feed-Line Impedance | 68 Ω |
| Simulation Tool | 4NEC2 |
| Simulation Engine | NEC2 |
| Environment | Free Space |
| Frequency Sweep | 77 points |
| Frequency Step | 100 MHz |
| Lowest Frequency | 400 MHz |
| Highest Frequency | 8 GHz |

---

## Design Concept

An LPDA consists of multiple dipole elements whose lengths and spacing change progressively along a boom.

The element dimensions follow a geometric scaling relationship controlled primarily by the **scaling factor (τ)** and **spacing factor (σ)**.

For this design:

- **τ = 0.90**
- **σ = 0.16**
- 35 dipole elements are used.
- The longest elements support the lower-frequency region.
- The shortest elements support the higher-frequency region.
- The antenna is fed through an alternating transmission-line arrangement along the boom.

This structure allows the antenna to operate over a much wider frequency range than a conventional single resonant dipole.

---

## Simulation Methodology

The antenna was modeled using the **NEC2 Method of Moments** implemented in 4NEC2.

The simulation workflow was:

1. Define the LPDA element geometry.
2. Apply the log-periodic scaling and spacing.
3. Model the boom and transmission-line connections.
4. Define the excitation at the feed point.
5. Set the free-space environment.
6. Perform a frequency sweep from **400 MHz to 8 GHz**.
7. Analyze:
   - Input resistance
   - Input reactance
   - SWR
   - Radiation pattern
   - Gain
   - Directivity
8. Study the antenna behavior at selected frequencies.

---

## Geometry

The final LPDA model contains **35 dipole elements** arranged along the boom.

The elements progressively decrease in length toward the high-frequency end.

The antenna is modeled using wire elements suitable for NEC2 simulation.

### Coordinate Arrangement

- Boom direction: X-axis
- Dipole elements: Z-axis
- Free-space electromagnetic environment
- Feed located at the high-frequency/smaller-element end

---

## Simulation Results

### SWR

The 4NEC2 simulation shows the characteristic frequency-dependent SWR variation of the LPDA.

The response contains multiple lower-SWR regions separated by periodic impedance variations. The SWR behavior is influenced by the element scaling, spacing, feed-line impedance, and finite number of elements.

The simulation covers the complete:

**400 MHz → 8 GHz**

frequency range.

---

### Input Impedance

The simulated input impedance varies considerably with frequency.

Both the resistance and reactance exhibit frequency-dependent variations as different elements become electrically active across the operating band.

This behavior is characteristic of a broadband multi-element antenna structure.

---

### Radiation Pattern

The LPDA produces directional radiation because the active region moves along the antenna as the operating frequency changes.

The radiation pattern was examined at selected frequencies using the 4NEC2 far-field analysis.

The main objective of the pattern analysis was to observe:

- Directionality
- Main-lobe behavior
- Front-to-back behavior
- Gain variation
- Frequency-dependent pattern changes

---

## Key Observations

- The LPDA provides operation over a very wide frequency range.
- The active region shifts along the array as frequency changes.
- Input impedance varies periodically with frequency.
- The radiation pattern remains directional over portions of the operating band.
- The antenna demonstrates the characteristic broadband behavior of a log-periodic structure.
- The finite number of elements influences the response near the frequency-band edges.

---

## Applications

A wideband directional LPDA can be used in applications such as:

- RF spectrum monitoring
- Broadband communication
- EMC/EMI measurements
- RF testing and measurement
- Signal monitoring
- Antenna measurements
- Research and development

---

## Software Used

### 4NEC2

**4NEC2** was used for:

- Antenna geometry modeling
- NEC2 electromagnetic simulation
- Frequency sweeps
- SWR analysis
- Input impedance analysis
- Far-field radiation-pattern analysis
- Gain and directivity analysis

---

## Project Structure

```text
LPDA-400MHz-8GHz/
│
├── README.md
│
├── NEC-Files/
│   ├── LPDA_Final.nec
│   └── *.nec
│
├── Simulation-Results/
│   ├── SWR/
│   ├── Impedance/
│   └── Radiation-Pattern/
│
├── Screenshots/
│   ├── Geometry/
│   ├── SWR/
│   ├── Impedance/
│   └── Radiation-Pattern/
│
└── Documentation/
    └── LPDA_Report.pdf
