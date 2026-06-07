# MALDI-TOF Antimicrobial Resistance Analysis

Analysis notebooks for rapid AMR prediction from MALDI-TOF mass spectra using
the [MaldiDeepKit](https://github.com/ettorerocchi/maldideepkit) framework on the
**Duroux DRIAMS** dataset.

## Dataset

Duroux D, Meyer P P, Visona G, Beerenwinkel N (2025). *Generalizable machine
learning models for rapid antimicrobial resistance prediction in unseen
healthcare settings.* GigaScience. [DOI:10.5524/102786](https://doi.org/10.5524/102786)

DRIAMS data originally from Weis et al. (2022), *Nature Medicine*.
CC0 1.0 Universal license.

## Notebooks

| # | Notebook | Description |
|---|----------|-------------|
| 0-0-1 | `duroux_analysis` | Full MaldiDeepKit pipeline — MLP, CNN, ResNet, Transformer classifiers, ensemble, uncertainty quantification |
| 0-0-2 | `LogisticAnalysis` | Bare-metal logistic regression baseline (single-site A2018, *S. aureus*) |
| 0-0-3 | `PooledLogisticAnalysis` | Pooled multi-site logistic regression (A+B+C+D, *E. coli*) |
| 0-0-4 | `MLPClassifier` | MaldiMLPClassifier pipeline matching the 0-0-2 LR baseline structure |

## Environment

```bash
conda activate MaldiTof
```

Requires:

- `maldideepkit >= 0.2.0`
- `maldiamrkit >= 0.15.0`
- `torch >= 2.0.0`
- `scikit-learn`, `pandas`, `numpy`, `matplotlib`

Each notebook generates reports and figures in its own `results_*/` subdirectory
and produces a `report.md` for cross-notebook comparison.
