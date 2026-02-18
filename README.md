# Space-Fluid-Quantum-Evidence
# Experimental Evidence of Black Hole-Generated Space: Quantum Ramsey Data

This repository contains the raw experimental data (JSON) and circuit codes (QASM) used to detect spatial fluid flow signals via IBM Quantum processors.

## 🌌 Theoretical Background
Based on the "Space Generation" model, supermassive black holes (SMBHs) act as sources of vacuum, creating a local flow of space fluid. This project utilizes superconducting qubits as high-precision probes to detect the phase shift induced by this flow relative to Earth's rotation.

## 🔬 Experimental Platform
- **Hardware**: `ibm_marrakesh` (126-qubit Eagle r3)
- **Method**: Ramsey Interferometry using $R_x(\pi/2)$ pulses and ultra-long delay times.
- **Combined Significance**: **6.6-sigma** deviation from vacuum baseline.

## 📁 Data Inventory

### 1. Q35: Scaling Series (Delay vs. Bias)
Investigating the linear/non-linear correlation of phase bias over varying durations ($\tau$).
- `Q35_scaling_1600ns.json` to `Q35_long_890000ns.json`
- Includes intermediate points: 4,981ns, 7,780ns, 10,577ns, 29,008ns, 89,000ns.

### 2. Q23: Temporal Modulation (9-Hour Shift)
Primary evidence of Earth-rotation coupling to the galactic vector field.
- `Q23_scaling_series.json`: Scaling from 600ns to 2,700ns.
- `Q23_baseline_2ms.json`: Primary 20,000 shot data (~2.034ms delay).
- `Q23_9h_shift_20k.json`: Verification of vector rotation after 9 hours.

### 3. Control Group
- `Control_ZeroDelay_20k.json`: 0ns delay baseline on Q23 to isolate hardware readout bias.

## ⚙️ How to Reproduce
The experimental circuits are provided in OpenQASM 2.0 format in the `/circuits` folder.
A representative job (e.g., `job-d6agn117ce2c73fe8sg0`) utilized a 4,068,000 dt delay to maximize sensitivity.



## 📊 Analysis
The phase bias $\phi$ is extracted from the $|1\rangle$ state population. 
Expected signal: A sinusoidal modulation with a ~24-hour period synchronized with the Earth's orientation relative to the galactic center.

## 🔗 Related Publication
For the full theoretical framework and astrophysical validation (102 galaxy sample), please refer to our ViXra paper:
**[Insert Your ViXra Link Here]**
