# Blind Engine Zero v1.0

Constant-free, deployable experimental core for **Hypothesis B′**.

## Design Mandate

- No hard-coded λ = 1.667, 5/3, 1.7333, 3.34, φ, or any preferred ratio.
- No theological / symbolic labels.
- No DOMINIQUE sequence or Alphabet Engine constants.
- Architecture is pure: `input → state → transform → evaluate → correct → memory`.
- Ratios, if any, must *emerge* from optimization — never be presupposed.
- Fully self-contained and runnable.

## Quick Start

```bash
python blind_engine_zero.py
```

This runs the blind architecture battery, ranks families by pure metrics, writes `blind_battery_report.json`, and demonstrates the incident-first identity model.

## Genetic-Code Test

```bash
cd genetic_code_test
python blind_genetic_test.py
```

Complete 64-codon table, 10 000 null models, positional asymmetry, blind ratio spectrum.

## What is tested

| Family              | Description                              |
|---------------------|------------------------------------------|
| random              | Unstructured baseline                    |
| binary              | 2-state                                  |
| 3-state             | 3-dimensional state                      |
| 4-state             | 4-dimensional state                      |
| 5-state             | 5-dimensional state                      |
| 3×4                 | Product space (3×4)                      |
| 4×3                 | Product space (4×3)                      |
| variable            | Variable-length style                    |
| adversarial         | Deliberately difficult                   |
| feedback            | Pure control-loop architecture           |
| incident            | Incident-first identity model            |

## Metrics (higher better after weighting)

- error (minimized)
- recovery
- information_efficiency
- noise_tolerance
- memory_stability
- prediction
- computational_cost (minimized)
- contradiction_handling

## Extending

1. Replace the synthetic observation generator with real data (genetic-code distance matrices, polyrhythm EEG features, control-system traces, etc.).
2. Implement the multiscale ladder (`multiscale_signature`) with domain-specific coarse-graining.
3. Add new architecture families by extending `ArchitectureFamily` and `make_architecture`.
4. Supply custom metric weights to `run_blind_battery`.

## License / Intent

Built to kill pattern recognition.  
Only what survives pure metrics remains.
