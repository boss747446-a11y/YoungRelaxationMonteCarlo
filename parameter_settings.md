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
satisfying the original sufficient condition (Theorem 1)** were obtained.

------------------------------------------------------------------------

## Fixed Design Parameters

### Controller poles

    [-1, -2]

### Observer poles

    [-2, -1]

The controller and observer pole locations were fixed to the above values for all
randomly generated systems. The corresponding controller and observer gains were
computed separately for each system. For each system, the same gains were used
when evaluating the sufficient conditions in Theorems 1 and 2.

### Scalar parameters

    β = 1e-1
    κ = 1e-15

------------------------------------------------------------------------

## Young Relaxation Parameters

### Search set for ρ₁

    {0.5, 1, 3, 5, 8.5, 10, 20, 50, 100, 200, 500}

### Search set for ρ₂

    {0.01, 0.05, 0.1, 0.2, 0.5, 1, 2}

For each system satisfying the original sufficient condition, all combinations of (ρ₁, ρ₂) were tested.
The Young-relaxed sufficient condition (Theorem 2) was regarded as feasible if at least one
parameter pair satisfied the corresponding LMI conditions.

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
  Original-condition feasible systems       1000
  Young-relaxed condition feasible            766
  Young-relaxed condition infeasible          234
  Feasibility retention ratio         76.6%
  Feasibility loss ratio              23.4%

------------------------------------------------------------------------

## Repository Contents

### Young_relaxation_feasibility_results.mat

Contains

-   Randomly generated system matrices
-   Controller gains determined separately for each system using the fixed controller poles
-   Observer gains determined separately for each system using the fixed observer poles
-   Feasibility results for the original and Young-relaxed sufficient conditions
-   Selected values of ρ₁ and ρ₂

### Young_relaxation_feasibility_summary.csv

Contains

-   Summary of the feasibility comparison for all systems satisfying the original sufficient condition.
