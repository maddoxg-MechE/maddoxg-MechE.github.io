# Physics-Informed Neural Network (PINN) Heat Transfer Solver

## Project Overview

This project investigates the use of physics-informed neural networks (PINNs) to solve heat transfer problems governed by differential equations. Traditional numerical approaches such as finite difference or finite element methods require discretizing the domain and solving large systems of equations. In contrast, PINNs embed the governing physical equations directly into the training process of a neural network, allowing the model to approximate solutions while satisfying the underlying physics.

The goal of this project is to implement a PINN model to solve a heat conduction problem and evaluate how accurately it predicts the temperature distribution across the domain. The neural network will be trained to minimize the residual of the governing heat equation while also satisfying the imposed boundary conditions.

## Methodology

The solver will be implemented in Python using the PyTorch machine learning framework. The neural network will take spatial coordinates as inputs and predict the corresponding temperature values. During training, the governing heat equation will be incorporated into the loss function so that the network learns solutions that satisfy the physics of heat conduction.

To validate the neural network results, the same physical scenario will also be simulated using finite element analysis in ANSYS Mechanical. This provides a numerical reference solution that can be compared directly against the PINN predictions. Temperature fields, convergence behavior, and overall solution accuracy will be evaluated between the two approaches.

## Objectives

The primary objective of this project is to explore whether physics-informed neural networks can produce accurate solutions to engineering heat transfer problems without relying on traditional discretization methods. By comparing the PINN solution to a finite element simulation, the project will assess the potential of machine learning approaches as alternative tools for solving physics-based engineering problems.

<div style="text-align:center;">
  <figure>
    <img src="/pinn1.png" style="max-height:400px; max-width:100%;">
    <figcaption>### Scenario being modeled in the PINN solver.</figcaption>
  </figure>
</div>

<div style="text-align:center; margin-top: 40px;">
  <figure>
    <img src="/pinn2.png" style="max-height:400px; max-width:100%;">
    <figcaption>### Predicted results from PINN (left: network setup, right: temperature prediction).</figcaption>
  </figure>
</div>
