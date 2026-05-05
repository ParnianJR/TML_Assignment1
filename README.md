# TML Assignment1: Membership Inference Attack

This repository contains the code to reproduce our best leaderboard result:
**TPR@5%FPR = 0.0558** on the private test set, using RMIA with γ=1.5, all-class reference matching, and per-class normalisation.
We used google colab to run the notebook, with T4 GPU.

You should place the following files in the working directory before running:

```
pub.pt
priv.pt
model.pt
```

## How to Reproduce

Open and run `code.ipynb` top to bottom. All steps are in order.

**1. Configuration** — seed, paths, and shadow model hyperparameters are set in the first config cell:

| Parameter | Value |
|---|---|
| Seed | 2026 |
| Number of shadow models | 10 |
| Shadow epochs | 80 |
| Shadow learning rate | 0.1 |
| Weight decay | 1e-3 |
| Label smoothing | 0.05 |
| Batch size | 256 |
| Subset ratio | 0.5 |

The final `submission.csv` is submitted to the server automatically by the last cell.
with 10 shadow models and 100 epoch, it took around 1 hour and half.
