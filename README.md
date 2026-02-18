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
Investigating the correlation of phase bias over varying durations ($\tau$).
- `Q35 201424ns 1k` (Initial scaling test)
- `Q35 2.046ms 20k` (Long delay scaling point)
- Scaling points include: 1,600ns, 4,981ns, 7,780ns, 10,577ns, 29,008ns, 89,000ns, and 890,000ns.

### 2. Q23: Temporal Modulation (Time-Series Evidence)
The core evidence showing the coupling between Earth's rotation and the galactic space fluid vector.
- **`Q23_2.034ms_30k_0218_KST0039`**: Baseline measurement ($P_1 \approx 0.4844$).
- **`Q23_2.034ms_20k_0218_KST0944`**: 9-hour shift showing maximum phase bias ($P_1 \approx 0.4772$).
- **`Q23_2.034ms_20k_0218_KST1558`**: 16:00 KST Rebound signal ($P_1 \approx 0.4868$), confirming sinusoidal modulation.

### 3. Control Group
- **`Q23_0ms_20k_0218_KST0920_Control`**: 0ns delay baseline on Q23 to isolate hardware readout bias ($P_1 \approx 0.4965$).

## ⚙️ How to Reproduce
The experimental circuits are provided in OpenQASM 2.0 format in the `/circuits` folder. 
A representative job (e.g., `job-d6agn117ce2c73fe8sg0`) utilized a **4,068,000 dt** delay to maximize sensitivity. 

To ensure the delay is correctly handled in QASM 2.0, use the `opaque delay(t) q;` declaration as shown in our source code.

## 📊 Analysis
The phase bias $\phi$ is extracted from the $|1\rangle$ state population. 

The observed shift from $0.4772$ to $0.4868$ over 6 hours is consistent with a sinusoidal modulation caused by the Earth's orientation relative to the galactic center.

## 🔗 Related Publication
For the full theoretical framework and astrophysical validation (102 galaxy sample), please refer to our ViXra paper:
**[Insert Your ViXra Link Here]**
