# AS-MPC on Namal Dam

## Overview
This repository contains scripts to run an Adaptive Scenario-based Stochastic Model Predictive Control (AS-MPC) for flood management at Namal Dam. The provided scripts implement various control schemes to analyze their performance in managing significant flood events.

## Requirements
- **Programming Language:** Julia 1.8.5
- **Optimization Solver:** Academic license for Mosek is required
- **Main Optimization Framework:** JuMP
- **Data Source:** Calibrated SWAT model-generated flow data

## Installing Required Julia Packages
To install the required Julia packages, run the following command in your Julia REPL:
```julia
using Pkg
Pkg.add(["LinearAlgebra", "Plots", "Dates", "Test", "Random", "Convex", "ECOS", "SCS", "Mosek", "ProgressMeter", "JuMP", "Statistics", "MosekTools", "Distributions", "Noise", "CSV", "DataFrames", "LaTeXStrings"])
```

## Data & Experiments
The input data comes from a calibrated SWAT model, which provides flow data for conducting hindcast experiments. The study focuses on three significant flood events:
- **September 1992**
- **Monsoon season of 2010**
- **Monsoon season of 2015**

### Control Schemes Implemented
The repository implements five different control schemes for comparison:
1. **Perfect Forecast (PF)-MPC**
2. **Single Forecast Deterministic (SFD)-MPC**
3. **Adaptive Scenario (AS)-MPC**
4. **Tree-Based (TB)-MPC**
5. **Adaptive Scenario Tree-Based (ASTB)-MPC**

## Running the Scripts
1. Ensure you have Julia 1.8.5 installed.
2. Install the required dependencies using Julia's package manager.
3. Run `AS_MPC_Dam.ipynb` using Jupyter Notebook or another Julia-supported IDE.
4. Use the plotting scripts to visualize results for different flood events.



## Contact
For any questions or collaborations, please reach out to the repository owner.


