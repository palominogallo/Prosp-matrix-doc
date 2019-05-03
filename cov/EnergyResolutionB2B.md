https://docdb.wlab.yale.edu/prospect/docs/0023/002315/006/Energy_Scale_Study_for_PROSPECT_For_Spectrum_Analysis_V3-3.pdf
page 19.

*./generateLvsEB2BEResCovMatrix input_ROOT_file detector_number sigma nToys*

In generateLvsEB2BEResCovMatrix.cc like:
```bash
vim aux/ToyCovExecs/generateLvsEB2BEResCovMatrix.cc
```

Change line 37
```c
double smearMean=Sigma = 1/sqrt(400) ~ 0.05
```

The *sigma* must be = 1/sqrt(408) - 1/sqrt(40) ~ 0.0005

```bash
>make generateLvsEB2BEResCovMatrix
>./generateLvsEB2BEResCovMatrix test.root inputs/CovMatrices_jose/SB2BLvsEEResCovMatrix_6.root 0.0005 1000

```

[README](../Readme.md)
