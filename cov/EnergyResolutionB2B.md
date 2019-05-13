## ./generateLvsEB2BEResCovMatrix input_ROOT_file output_ROOT_file sigma nToys

https://docdb.wlab.yale.edu/prospect/docs/0023/002315/006/Energy_Scale_Study_for_PROSPECT_For_Spectrum_Analysis_V3-3.pdf
page 19.

1. In generateLvsEB2BEResCovMatrix.cc like:
```bash
vim aux/ToyCovExecs/generateLvsEB2BEResCovMatrix.cc
```

2. Change line 37
```c
double smearMean=Sigma = 1/sqrt(400) ~ 0.05
```

3. The *sigma* must be = 1/sqrt(408) - 1/sqrt(40) ~ 0.0005

## Run
```bash
>make generateLvsEB2BEResCovMatrix
>./generateLvsEB2BEResCovMatrix test.root inputs/CovMatrices_jose/SB2BLvsEEResCovMatrix_6.root 0.0005 1000

```

[README](../Readme.md)
