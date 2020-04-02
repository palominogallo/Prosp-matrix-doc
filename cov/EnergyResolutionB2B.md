## SB2BERES

**SignalB2BERESCovFile101**

https://docdb.wlab.yale.edu/prospect/docs/0028/002815/001/main.pdf
page 22.

1. In generateLvsEB2BEResCovMatrix.cc like:
```bash
vim aux/ToyCovExecs/generateLvsEB2BEResCovMatrix.cc
```

2. Change line 37
```c
double smearMean= 1/sqrt(325) ~ 0.05
```

3. The *sigma* must be = 1/sqrt(350) - 1/sqrt(325) ~ 0.0020

## Run
```bash
>make generateLvsEB2BEResCovMatrix
>./generateLvsEB2BEResCovMatrix test.root inputs/CovMatrices_jose/SB2BLvsEEResCovMatrix_6.root 0.0020 1000

```

[README](../Readme.md)
