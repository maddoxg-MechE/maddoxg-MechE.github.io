# Matlab Project: Solution of 2nd order Non-linear ODE 

## Project Report

Simulated the nonlinear dynamics of a simple pendulum by solving the second-order ODE for angular position and angular velocity using MATLAB’s 
ode45 over a 0–200 s interval. Computed the nonlinear period using adaptive Gauss–Kronrod quadrature (quadgk) and used that result to verify the 
time-domain ODE solution by comparing measured oscillation periods from the numerical response. Evaluated solver accuracy by running ode45 with 
two tolerances (10⁻³ and 10⁻⁶), extracting θ(t) and θ˙(t) at specific times via interpolation, and generating time histories and phase (Poincaré) 
plots. Repeated the full analysis for two physical cases—no drag and a nonzero drag coefficient—to observe how damping alters amplitude decay 
and phase-space behavior.

[Open the PDF in a new tab](/Project_9.pdf)

<iframe
  src="/Project_9.pdf"
  width="100%"
  height="1100"
  style="border: none;"
></iframe>
