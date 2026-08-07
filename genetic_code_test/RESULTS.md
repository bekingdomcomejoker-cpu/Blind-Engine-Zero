# Blind Genetic-Code Test Results

## Codon Table Verification
- 64 codons
- 21 unique labels (20 AA + stop)
- Leucine block complete: UUA UUG CUU CUC CUA CUG
- Stops: UAA UAG UGA

## Robustness vs Nulls (10 000 randomizations)

### Block-preserving null
| Property    | Standard | Null mean | Lower-tail p |
|-------------|----------|-----------|--------------|
| Hydropathy  | 2.049    | 2.640     | 0.01 %       |
| Volume      | 26.785   | 29.147    | 2.57 %       |
| Polarity    | 1.877    | 2.412     | 0.00 %       |

### Unrestricted null
| Property    | Standard | Null mean | Lower-tail p |
|-------------|----------|-----------|--------------|
| Hydropathy  | 2.049    | 3.425     | 0.00 %       |
| Volume      | 26.785   | 37.391    | 0.00 %       |
| Polarity    | 1.877    | 3.043     | 0.00 %       |

## Positional Asymmetry (Standard Code)

Synonymous substitution fractions:
- Position 1: 4.37 %
- Position 2: 0.00 %
- Position 3: 68.85 %

## Blind Ratio Spectrum (nearest frozen candidate)

| Measured ratio              | Value  | Nearest | Distance |
|-----------------------------|--------|---------|----------|
| polarity_pos2 / pos1        | 1.6896 | **5/3** | 0.0229 (1.38 %) |
| volume_pos2 / pos1          | 1.1824 | 4/3     | 0.1509 |
| hydropathy_pos2 / pos1      | 2.2643 | 2       | 0.2643 |

**Key observation**: polarity cost ratio pos2/pos1 lands 1.38 % from 5/3.
Volume ratio lands nearer 4/3. No single ratio dominates all metrics.

## Conclusion for Hypothesis B

- Genetic code is strongly non-random under both null models (survives).
- Positional hierarchy is extreme (pos2 zero synonymy, pos3 high synonymy).
- 5/3 appears as nearest candidate for one independent ratio (polarity).
- 4/3 appears for another (volume).
- Neither is universal; both remain candidate observations only.

Full machine-readable data: `genetic_blind_report.json`
