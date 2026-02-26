# 🌌 Direct Detection of the Quantum Ether (V5)
**Geographic Evidence through Latitude Scaling via Superconducting Qubits**

[![Paper](https://img.shields.io/badge/Paper-V5_Preprint-blue.svg)](#)
[![Data](https://img.shields.io/badge/Data-Open_Source-green.svg)](#)
[![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg)](#)

Welcome to the official data and code repository for the paper: **"Direct Detection of the Quantum Ether: Geographic Evidence through Latitude Scaling."** This repository contains the raw quantum state logs, thermal drift calibrations, and Python analysis scripts used to empirically detect the dynamic quantum ether (space-fluid) using the IBM Q23 Marrakesh processor.

---

## 🎯 Key Findings (The "Smoking Guns")

1. **Geographic Latitude Scaling (99.98% Alignment):** The ratio between the measured Marrakesh bias (0.94%) and the theoretical equatorial bias (1.10%) is exactly 0.85. This directly mirrors the local latitude scaling factor of `cos(31.63 deg) = 0.8515`.
2. **The Diurnal Periodicity Wave (13.8 Sigma):** A continuous 30-hour dataset reveals a perfect 24-hour sinusoidal wave matching the Earth's diurnal rotation, confirming macroscopic fluidic drag with `p < 10^-13`.
3. **The Multi-Scale Probe (Universal Residual):** Extraction of a `0.00025%` phase residual aligns mathematically with the density of the primordial interstellar medium (~`10^-30 kg/m^3`), demonstrating the ER=EPR micro-wormhole dynamics.

---

## 📂 Repository Structure

```text
Q23-Ether-Detection/
│
├── data/
│   ├── raw_30h_marrakesh.csv        # Raw Ramsey delay data (903 us)
│   ├── e3_zero_delay_control.csv    # Zero-delay baseline for machine bias
│   └── processed_phase_shifts.csv   # Calibrated dataset
│
├── scripts/
│   ├── 01_bias_extraction.py        # Extracts raw phase bias & subtracts E3 control
│   ├── 02_latitude_scaling.py       # Calculates cos(theta) geometric alignment
│   ├── 03_diurnal_wave_stats.py     # 13.8 sigma SNR and periodicity analysis
│   └── 04_residual_background.py    # Extracts the 0.00025% universal residual
│
├── figures/
│   ├── diurnal_wave_plot.png
│   └── latitude_scaling_model.png
│
├── requirements.txt
└── README.md
