# Physics-Informed Neural Network for Phase-Change Heat Transfer in Additive Manufacturing

## Project Overview

This project investigates the application of **Physics-Informed Neural Networks (PINNs)** to solve transient heat transfer problems involving phase change. A one-dimensional Stefan problem representative of additive manufacturing was implemented in PyTorch and validated against finite element method (FEM) solutions.

Unlike traditional numerical approaches that require mesh generation and repeated discretization, PINNs incorporate the governing differential equations directly into the loss function. The neural network learns the temperature field while simultaneously satisfying the underlying physics and imposed boundary conditions.

<div style="text-align:center;">
  <figure>
    <img src="/pinn1.png" style="max-height:400px; max-width:100%;">
    <figcaption>
    </figcaption>
  </figure>
</div>

The study focused on the influence of boundary-condition enforcement strategies and collocation density on training stability and solution accuracy. Two approaches were investigated:

- **Hard boundary conditions**, where Dirichlet boundary values are embedded directly into the network output.
- **Soft boundary conditions**, where boundary values are enforced through penalty terms in the loss function.

Results demonstrated that hard boundary enforcement produced significantly more stable training and improved accuracy.

## Methodology

The solver was developed in **Python using PyTorch** and modeled a one-dimensional graphite-aluminum domain undergoing phase change. The governing enthalpy form of the transient heat equation was enforced through automatic differentiation.

### PINN Architecture

- Four fully connected hidden layers
- 200 neurons per layer
- tanh activation functions
- Approximately 123,000 trainable parameters

### Training Procedure

Training was performed in two stages:

1. Pre-training using the initial temperature field.
2. Physics-informed optimization using:
   - PDE residual loss
   - Initial condition loss
   - Boundary condition losses (soft BC model)

Optimization employed both the Adam optimizer and L-BFGS.

### Finite Element Validation

A separate finite element solver was implemented to provide reference solutions and perform mesh refinement studies. Temperature fields, phase-interface locations, and relative L₂ errors were compared against the PINN predictions.

## Key Results

### Hard Boundary Conditions Outperformed Soft Boundary Conditions

- Hard-BC PINN relative error: **0.9 × 10⁻³**
- Soft-BC PINN relative error: **2.0 × 10⁻³**

Hard boundary enforcement produced smoother convergence and avoided the optimization instabilities observed in the soft-BC formulation.

### Comparison with FEM

| Resolution | FEM Error | Hard-BC PINN Error |
|------------|----------:|------------------:|
| Nx = 50 | 3.6×10⁻² | 1.1×10⁻³ |
| Nx = 100 | 9.1×10⁻³ | 1.0×10⁻³ |
| Nx = 150 | 4.1×10⁻³ | 1.0×10⁻³ |
| Nx = 200 | 2.3×10⁻³ | 0.9×10⁻³ |

At coarse resolutions, the PINN outperformed FEM by more than an order of magnitude while avoiding explicit mesh generation. Increasing the number of collocation points beyond moderate levels produced only marginal improvements in accuracy.

## Major Findings

- Hard boundary enforcement was significantly more robust than soft boundary enforcement.
- PINNs accurately captured both the temperature field and phase-interface evolution.
- Training stability depended strongly on normalization and loss balancing.
- Increasing collocation density beyond 10,000 points yielded little improvement in accuracy.
- The hard-BC PINN achieved relative errors below 10⁻³ while avoiding traditional mesh generation.


## Technical Report and Presentation

The complete technical report and presentation are available below.

### Research Paper

[Open the Research Paper (PDF) in a new tab](/EML_5360_Project_Paper.pdf)

<iframe
  src="/EML_5360_Project_Paper.pdf"
  width="100%"
  height="1100"
  style="border: none;"
></iframe>

### Project Presentation

<iframe
  src="./EML_5360_Project_Presentation.pdf"
  width="100%"
  height="700"
  style="border:none;">
</iframe>

[Download the PowerPoint Presentation](/EML_5360_Project_Presentation.pptx)

<iframe
  src="https://view.officeapps.live.com/op/embed.aspx?src=https://maddoxg-meche.github.io/EML_5360_Project_Presentation.pptx"
  width="100%"
  height="700"
  frameborder="0">
</iframe>
