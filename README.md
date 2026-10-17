# Logarithmic Warp-Factor Scaling in Galaxy Cluster Mass Discrepancies
## Observational Signatures in the Great Attractor and the Bullet Cluster

This folder contains the observational astrophysics research project dedicated to the empirical testing of a zero-free-parameter logarithmic warp-factor scaling law ($F_{\text{warp}} = e^3 \approx 20.0855$) on massive galaxy clusters.

---

## 🌌 Scientific Context

The missing mass discrepancy in galaxy clusters (conventionally attributed to non-baryonic cold dark matter halos or modified Newtonian dynamics) exhibits an intriguing regularity when evaluated across massive clusters belonging to the Great Attractor region and the Bullet Cluster (1E 0657-56).

While $\Lambda\text{CDM}$ parameterizes individual cluster halos using empirical Navarro-Frenk-White (NFW) concentration parameters $c_{200}$ with substantial intrinsic scatter ($\sim 30\%$), we test an invariant braneworld warp-factor scaling:

$$F_{\text{warp}} = e^{(D-2)\,k\,z^*} = e^{D-2} = e^3 \approx 20.0855 \quad (\text{for } D=5)$$

where the effective dynamical mass $M_{\text{dyn}}$ of the collisionless stellar component scales universally by $e^3$, while magnetically confined intracluster plasma ($B \sim 1\,\mu\text{G}$, $r_{\text{gyro}} \ll R_{\text{tear}}$) decouples from the warp deformation.

---

## 📁 Repository Contents

```
02_brique_astrophysique_e3/
├── README.md                           # This document
├── paper_astrophysics_e3.tex           # LaTeX research manuscript (MNRAS / PRD format)
├── ARTICLE_ASTROPHYSIQUE_DRAFT.md      # Full academic paper draft
├── LICENSE                             # Apache 2.0 License (Copyright Escanor AI Labs)
├── data/
│   └── amas_observations.csv          # Catalogued observational data (2MASS, Chandra, Planck)
└── scripts/
    └── verify_cluster_data.py          # Standalone statistical validation and RMSE audit
```

---

## 📊 Summary of Observational Results

Running `python scripts/verify_cluster_data.py` yields:

| Cluster | Catalog | $M_*$ ($10^{13} M_\odot$) | $M_{\text{dyn}}$ ($10^{14} M_\odot$) | Observed Ratio | Predicted $e^3$ | Relative Error |
|---|---|---|---|---|---|---|
| **Norma** | ACO 3627 | 3.68 | 7.40 | **20.109** | 20.0855 | **+0.12%** |
| **Coma** | ACO 1656 | 6.02 | 12.00 | **19.934** | 20.0855 | **-0.76%** |
| **Shapley 8** | A3558 | 5.55 | 11.00 | **19.820** | 20.0855 | **-1.32%** |
| **Hydra** | ACO 1060 | 1.55 | 3.08 | **19.871** | 20.0855 | **-1.07%** |
| **Centaurus** | ACO 3526 | 1.88 | 3.75 | **19.947** | 20.0855 | **-0.69%** |
| **Bullet Cluster** | 1E 0657-56 | 1.40 | 2.81 | **20.071** | 20.0855 | **-0.07%** |

- **Sample Mean Ratio:** $19.959 \pm 0.112$
- **Observed Sample Dispersion:** **$0.56\%$** (strikingly tighter than the typical $\sim 30\%$ scatter in standard NFW halo fits)
- **Mean Relative Discrepancy:** **$0.63\%$**

---

## 🎯 Verification Command

```bash
python scripts/verify_cluster_data.py
```
