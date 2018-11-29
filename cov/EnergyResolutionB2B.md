https://docdb.wlab.yale.edu/prospect/docs/0023/002315/006/Energy_Scale_Study_for_PROSPECT_For_Spectrum_Analysis_V3-3.pdf
page 19.

Change the line 37 in generateLvsEB2BEResCovMatrix.cc
```c
double smearMean=Sigma = 1/sqrt(400) ~ 0.05
```

The Sigma = 1/sqrt(408) - 1/sqrt(40) ~ 0.0005
```bash
>make generateLvsEB2BEResCovMatrix
>./generateLvsEB2BEResCovMatrix stats_6.root inputs/CovMatrices_jose/SB2BLvsEEResCovMatrix_6.root 0.0005 1000

```

[README](../Readme.md)
