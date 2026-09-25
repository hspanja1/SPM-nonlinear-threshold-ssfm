# Self-Phase Modulation (SPM) and Nonlinear Threshold in Single-Channel Optical Systems

## Overview
This project investigates the impact of nonlinear effects — particularly **Self-Phase Modulation (SPM)** caused by the Kerr effect — on the performance of single-channel optical communication systems. A numerical simulation model based on the **Split-Step Fourier Method (SSFM)** was developed to model pulse propagation through multiple fiber spans with EDFA amplification.

The simulation includes:
- Linear effects: chromatic dispersion and fiber loss
- Nonlinear effects: self-phase modulation (SPM)
- Amplifier noise: ASE (Amplified Spontaneous Emission) from EDFA

By analyzing **EVM (Error Vector Magnitude)** and **BER (Bit Error Rate)** as functions of input peak power, the **nonlinear threshold** of the system was identified — the power level beyond which nonlinear effects begin to dominate and degrade signal quality.

## Key Results
- System performance initially improves with increasing input power (due to improved OSNR)
- Beyond a certain optimal power (~11–12 mW in this simulation), Kerr-induced nonlinearities dominate and degrade EVM/BER
- Theoretical nonlinear phase threshold (φ_NL = 1 rad) occurs at ≈ 8 mW input power

## Methods
- **Nonlinear Schrödinger Equation (NLSE)** for pulse propagation
- **Split-Step Fourier Method (SSFM)** for numerical solving
- QPSK modulation with RRC pulse shaping
- EDFA amplification with ASE noise modeling

## Repository Contents
- `notebook.ipynb` — full simulation code (Google Colab)
- `figures/` — generated plots (EVM, BER, OSNR-like metric, spectral broadening, nonlinear threshold)
- `report.pdf` — full project report (in Bosnian)
- `requirements.txt` — Python dependencies

## How to Run
1. Open the notebook in [Google Colab](https://colab.research.google.com) or locally with Jupyter
2. Install dependencies:
```bash
   pip install -r requirements.txt
```
3. Run all cells to reproduce the simulation and plots

