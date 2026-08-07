# Synthetic Architecture Sweep — Track A Results

**Engine:** SyntheticArchitectureSweep-v1  
**Date:** 2026-08-08  
**Constraint:** No preferred ratios. Ranking by robustness / log(capacity).

## Full 14-Architecture Table

| Rank | Architecture | Capacity (A^L) | Robustness | Above Random | Robustness / log(C) |
|------|--------------|----------------|------------|--------------|---------------------|
| 1    | **3×2**      | 9              | 0.5556     | +0.0556      | **0.02528**         |
| 2    | 6×2          | 36             | 0.1389     | +0.0389      | 0.01085             |
| 3    | **4×3**      | 64             | 0.0625     | +0.0099      | 0.00237             |
| 4    | 6×3          | 216            | 0.0173     | +0.0017      | 0.00031             |
| 5    | 5×3          | 125            | 0.0280     | +0.0010      | 0.00020             |
| 6    | 5×4          | 625            | 0.0062     | +0.0009      | 0.00013             |
| 7    | 2×2          | 4              | 0.5000     | 0.0000       | 0.00000             |
| 8    | 2×3          | 8              | 0.5000     | 0.0000       | 0.00000             |
| 9    | 4×2          | 16             | 0.2500     | 0.0000       | 0.00000             |
| 10   | 4×4          | 256            | 0.0124     | −0.0008      | −0.00014            |
| 11   | 3×4          | 81             | 0.0278     | −0.0139      | −0.00316            |
| 12   | 3×3          | 27             | 0.1111     | −0.0139      | −0.00421            |
| 13   | 5×2          | 25             | 0.0800     | −0.0629      | −0.01953            |
| 14   | 2×4          | 16             | 0.1875     | −0.0625      | −0.02254            |

## 4×3 Specifics

- Capacity: **64**
- Robustness: 0.0625
- Above random baseline: +0.0099
- Capacity-normalized score: 0.00237
- **Rank: 3 / 14**

## Interpretation

Under this pure synthetic construction (random class assignment, single-symbol mutation robustness, capacity-normalized):

> **4×3 did not emerge as the universal optimum.**

Smaller alphabets with short sequence lengths scored higher on the normalized metric. 4×3 is respectable (top quartile) but not exceptional.

### Consequence for Hypothesis B

The claim “4 symbols × 3 positions is intrinsically optimal” **fails** this capacity-normalized synthetic test.

The surviving, more defensible claim is:

> Alphabet size and sequence length jointly create a capacity / redundancy / error-tolerance tradeoff.

Biology’s selection of the 4×3 point therefore cannot be explained by raw combinatorial optimality alone.

## Method Notes

- No DNA, amino acids, theology, or preferred numerical constants were used.
- Ranking criterion: `robustness_above_random / log(capacity)`
- Full machine-readable data: `synthetic_sweep_report.json`
