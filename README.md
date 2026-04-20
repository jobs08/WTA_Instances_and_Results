# WTA Instance Format

Each instance is stored as a plain-text file with labeled sections.

The current format contains the following blocks:
----------------------------------------------------------------
W, T, Omega: numbers of weapons, targets, and scenarios.

theta_vals: target damage thresholds.

cost: unit assignment costs of weapon types.

resources: available quantities of each weapon type.

prob_destroy (W x T): damage probability matrix.

alpha_scenarios (Omega x W x T): scenario-dependent availability matrices.

slack cost: unit penalty cost for damage shortfall.

The file and folder names are simplified to directly indicate the instance scale.
For example, W10T50 denotes instances with 10 weapons and 50 targets, and W10_T50_S50_1.txt denotes the first instance with 10 weapons, 50 targets, and 50 scenarios.

## Example

```text
# W T Omega
10 50 50

# theta_vals
0.738 0.702 0.789 ...

# cost
30 22 35 36 31 28 64 60 67 72

# resources
15 15 15 15 15 15 15 15 15 15

# prob_destroy (W x T)
0.519 0.435 0.633 ...
0.697 0.570 0.506 ...
...

# alpha_scenarios (Omega x W x T)
# scenario 1
0 1 1 ...
1 1 1 ...
...
# scenario 2
...

# slack cost
10000
```
