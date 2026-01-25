# Matlab Project: Solving Non-Linear Equations Using Newton-Raphson

## Project Report

### This project focused on solving a system of nonlinear simultaneous equations arising from the finite-difference modeling of one-dimensional heat conduction in a bar with temperature-dependent thermal conductivity. The governing equations were formulated using a discretized energy balance with conductivity varying linearly with temperature, resulting in a coupled nonlinear system for the nodal temperatures. The nonlinear system was solved using the Newton–Raphson method implemented in MATLAB, with the Jacobian matrix evaluated at each iteration using first-order backward finite-difference approximations. Convergence was enforced using both residual and iterative norm criteria. The solution was compared against a corresponding linearized case by setting the nonlinear conductivity coefficient to zero, allowing direct evaluation of the impact of temperature-dependent material properties on the thermal response.

[Open the PDF in a new tab](/Project_5.pdf)

<iframe
  src="/Project_5.pdf"
  width="100%"
  height="1100"
  style="border: none;"
></iframe>

