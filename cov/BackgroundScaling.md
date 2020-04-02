## BSCALE

**BACKGROUNDSCALECOVFILE101**

The DocDB 2377
Plot 9 seems the variation is  not more than 0.2%. this plot is reference.

Edit the file **generateLvsEScaleCovMatrix** L 52
```bash
vim aux/ToyCovExecs/generateLvsEScaleCovMatrix.cc
```
This LvsEScaleCovMatrix generator also works for Bkg

hName.Form("LvsENull%i",101); -> hName.Form("BkgRxOnLvsE%i",101);

```bash
>make generateLvsEScaleCovMatrix
>./generateLvsEScaleCovMatrix test.root inputs/CovMatrices/BLvsEScaleCovMatrix.root 0.002 1000
```
[README](../Readme.md)
