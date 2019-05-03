# Covariance Matrix Generation 

| Matrix | Value | Uncertainty | Source | Process Time |
| --- | --- | --- | --- | --- | --- |
| Background Norm | 99.121% | 1% | [DocDB 2509](https://docdb.wlab.yale.edu/prospect/ShowDocument?docid=2509)| Non-PG4 toys | |
| [Energy Loss](cov/EnergyLoss.md) | - | 8 KeV | [DocDB 2503](https://docdb.wlab.yale.edu/prospect/ShowDocument?docid=2503)| Non-PG4 toys | ~1 min |
| [B2B Energy Loss](cov/EnergyLossB2B.md) | - | 8 KeV | Assume same as the full detector | Non-PG4 toys | ~60 mins |
| [Baseline uncertainty](cov/BaselineUncertainty.md) | 7932 mm | 100 mm | [DocDB 2229](https://docdb.wlab.yale.edu/prospect/ShowDocument?docid=2229) | Non-PG4 toys | |
| [B2B Energy Resolution](cov/EnergyResolutionB2B.md) | 400 PE/MeV | 8 PE/MeV | [DocDB 2315 v6](https://docdb.wlab.yale.edu/prospect/ShowDocument?docid=2315)  | Non-PG4 toys | |

I will need the [OscSens CovMatrix](https://github.com/PROSPECT-collaboration/OscSens_CovMatrix)
The input file needed is the output from runOscChain ?
