# Matlab Project: 1st order ODE Solver for circuit

## Project Report

### Modeled the discharge of an RC circuit by formulating and solving the first-order ODE for capacitor voltage V(t), which is also analogous to the transient cooling response of a thermocouple bead. Implemented the explicit Euler method in MATLAB over 𝑡∈[0,10] t∈[0,10] s using multiple time steps and compared the numerical results against the exact analytical solution to evaluate stability and time-step sensitivity. Extracted solution values at specific times using linear interpolation when the time grid did not align with requested points. Then solved the same ODE using MATLAB’s ode45 with both default and tightened tolerances, comparing accuracy and convergence behavior between fixed-step (Euler) and adaptive-step (ode45) approaches..

[Open the PDF in a new tab](/Project_8.pdf)

<iframe
  src="/Project_8.pdf"
  width="100%"
  height="1100"
  style="border: none;"
></iframe>
