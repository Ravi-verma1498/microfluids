🧪 Microfluidic Flow Simulation & Sensitivity Analysis
This repository contains simulation code and analysis tools for modeling pressure-driven laminar flow in microchannels using both 1D semi-analytical and 2D finite volume methods (FVM). The project compares water and blood flow behavior, focusing on non-Newtonian effects and fluid mixing, and performs sensitivity analysis to identify dominant parameters.
📌 Project Overview
Microfluidic systems are widely used in biomedical and chemical applications. This project aims to:
- Simulate pressure-driven flow for water and blood in microchannels
- Implement 1D models for non-Newtonian flow and fluid mixing
- Validate with 2D FVM simulations
- Perform sensitivity analysis (OAT and Morris methods) to identify key parameters

🔬 Methodology
1D Models
- Non-Newtonian Flow: Carreau–Yasuda viscosity model, root-finding for shear rate, velocity integration
- Fluid Mixing: Advection–diffusion equation solved via Fourier series, AMI used for quantifying mixing
2D FVM Simulation
- Solves Navier–Stokes and Pressure Poisson equations
- Structured mesh with no-slip boundary conditions
- Compares water (Newtonian) and blood (high viscosity) flow profiles
Sensitivity Analysis
- Stage 1: One-at-a-time (OAT) perturbation
- Stage 2: Morris method for global screening
- Outputs: Centerline velocity (Uₘₐₓ), flow rate (Q), and Absolute Mixing Index (AMI)
📊 Key Findings
- Zero-shear viscosity (μ₀) is the most influential parameter for non-Newtonian flow
- Channel width and inlet speed dominate mixing efficiency
- 1D models offer fast, interpretable insights for design optimization
🚀 Getting Started
Prerequisites
Install dependencies using:
pip install -r requirements.txt


Run Simulations
# Run 1D non-Newtonian flow
python 1D_NonNewtonian/carreau_solver.py

# Run 2D FVM simulation
python 2D_FVM_Simulation/fvm_solver.py


📈 Sample Outputs
- Velocity profiles for blood vs. water
- Tornado plots showing parameter sensitivities
- AMI evolution along the channel

📎 Reference
This work builds on prior studies of microfluidic modeling and extends them with systematic sensitivity analysis. For more details, see the project presentation: CLL770_Project_final.pptx

