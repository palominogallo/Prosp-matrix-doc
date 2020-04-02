# Installation PG4 and P2X
* [In Borax](install/borax.md)

# Covariance Matrix Generation

| Matrix | Value | Uncertainty | Source | Toy | Process Time |
| --- | --- | --- | --- | --- | --- |
| [B2B Energy Scale ](cov/EnergyScaleB2B.md) | 1 | 0.007 | [DocDB 2363](https://docdb.wlab.yale.edu/prospect/docs/0023/002363/002/EScaleUpdate_05_31_18.pdf) | Non-PG4 toys | ~ 90 mins |
| [B2B Energy Resolution](cov/EnergyResolutionB2B.md) | 400 PE/MeV | 8 PE/MeV | [DocDB 2815-v1](https://docdb.wlab.yale.edu/prospect/docs/0028/002815/001/main.pdf)  | Non-PG4 toys | ~2 mins |
| [Background Norm](cov/BackgroundNorm.md) | 99.121% | 1% | [DocDB 2509](https://docdb.wlab.yale.edu/prospect/ShowDocument?docid=2509)| Non-PG4 toys | |
| [Energy Loss](cov/EnergyLoss.md) | - | 8 KeV | [DocDB 2503](https://docdb.wlab.yale.edu/prospect/ShowDocument?docid=2503)| Non-PG4 toys | ~1 min |
| [B2B Energy Loss](cov/EnergyLossB2B.md) | - | 8 KeV | Assume same as the full detector | Non-PG4 toys | ~60 mins |
| [Baseline uncertainty](cov/BaselineUncertainty.md) | 7932 mm | 100 mm | [DocDB 2229](https://docdb.wlab.yale.edu/prospect/ShowDocument?docid=2229) | Non-PG4 toys | |
| [Background Scaling](cov/BackgroundScaling.md) | | 0.002 | [DocDB 2377](https://docdb.wlab.yale.edu/prospect/docs/0023/002377/002/bipo-analysis%281%29.pdf) | Non-PG4 toys | ~1 min |
| [B2B Volume](cov/VolumeB2B.md) | | | | Non-PG4 toys | ~1min |
| [Non Lin Energy](cov/NonLinearEnergy.md) | | | | PG4 toys | ~ min |

I will need the [OscSens CovMatrix](https://github.com/PROSPECT-collaboration/OscSens_CovMatrix)
The input file needed is the output from runOscChain ?
