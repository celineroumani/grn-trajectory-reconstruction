# Gene-Regulatory Trajectory Reconstruction

This repository contains the MATLAB code for the study *Effect of Governing ODE Constraints on Gene-Regulatory Trajectory Reconstruction under Sparse and Noisy Observations* by Celine Roumani and Hazem Harb.

The study compares a physics-informed neural network (PINN) with a matched unregularized neural network, three L2-regularized variants, and a direct ODE fit. The script generates synthetic gene-expression data for a two-gene mutual-repression system and evaluates four observation counts and four noise levels, with ten matched repetitions per condition.

## Requirements

- MATLAB R2025b
- Deep Learning Toolbox for neural-network training
- Optimization Toolbox for the direct ODE fit using `lsqnonlin`

## Reproduce the results

Open the repository folder in MATLAB and run:

```matlab
GRN_Revision(1)
```

The script generates the synthetic observations, trains the neural networks, fits the direct ODE baseline, and exports the results. No external dataset is required. If a run is interrupted, rerun the script from the same folder to resume from completed checkpoints.

## Outputs

The script creates `GRN_Revision_Results/` alongside `GRN_Revision(1).m`. The `Summary/` subfolder contains the run-level results, condition summaries, paired RMSE differences and confidence intervals, baseline comparisons, and training diagnostics. It also contains the three manuscript figures in PDF, PNG, and MATLAB FIG formats.
