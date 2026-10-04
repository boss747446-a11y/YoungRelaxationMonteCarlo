# Monte Carlo Feasibility Dataset

This repository contains the dataset used for the Monte Carlo feasibility study reported in the paper.

Contents

- Randomly generated system matrices
- Controller gains determined by fixed pole placement
- Observer gains determined by fixed pole placement
- Feasibility results for the original sufficient condition (Theorem 1)
- Feasibility results for the Young-relaxed sufficient condition (Theorem 2)
- Simulation parameters

For all systems, the controller poles were fixed at ${-1,-2}$ and the observer poles were fixed at ${-2,-1}$. The corresponding controller and observer gains were computed separately for each randomly generated system and were kept identical when comparing the sufficient conditions in Theorems 1 and 2.
