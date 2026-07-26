# Parameter Settings

## Monte Carlo Feasibility Study

This repository contains the parameter settings used for the Monte Carlo
feasibility study reported in the manuscript.

### Random System Generation

-   System order: **n = 2**
-   Number of inputs: **m = 1**
-   Number of outputs: **p = 1**

The system matrices were generated as

-   **A ∈ ℝ\^(2×2)**
-   **B ∈ ℝ\^(2×1)**
-   **C ∈ ℝ\^(1×2)**

whose entries were independently sampled from the standard normal
distribution.

Only **controllable** and **observable** systems were retained.

A total of **22,235** random systems were generated until **1000 systems
satisfying the original BMI condition (Theorem 1)** were obtained.

------------------------------------------------------------------------

## Fixed Design Parameters

### Controller poles

    [-1, -2]

### Observer poles

    [-2, -1]

### Scalar parameters

    β = 1e-1
    κ = 1e-15

------------------------------------------------------------------------

## Young Relaxation Parameters

### Search set for ρ₁

    {0.5, 1, 3, 5, 8.5, 10, 20, 50, 100, 200, 500}

### Search set for ρ₂

    {0.01, 0.05, 0.1, 0.2, 0.5, 1, 2}

For each BMI-feasible system, all combinations of (ρ₁, ρ₂) were tested.
The Young-relaxed LMI condition was regarded as feasible if at least one
parameter pair satisfied the LMI conditions.

------------------------------------------------------------------------

## Software

-   MATLAB
-   YALMIP
-   SeDuMi

------------------------------------------------------------------------

## Summary of Results

  Item                                Value
  -------------------------------- --------
  Total random systems generated     22,235
  BMI-feasible systems collected       1000
  Young-relaxed LMI feasible            766
  Young-relaxed LMI infeasible          234
  Feasibility retention ratio         76.6%
  Feasibility loss ratio              23.4%

------------------------------------------------------------------------

## Repository Contents

### BMI_LMI_conservatism_results.mat

Contains

-   Randomly generated system matrices
-   Fixed controller gains
-   Fixed observer gains
-   BMI/LMI feasibility results
-   Selected values of ρ₁ and ρ₂

### BMI_LMI_conservatism_summary.csv

Contains

-   Summary of the feasibility comparison for all BMI-feasible systems.
