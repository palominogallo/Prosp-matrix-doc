I got the information from Danielle Berish.
I had to modify the file to have Count vs Segment in one 1D histogram. The operation only takes the error from each point
Edit the file **generateLvsEB2BVolCovMatrix** L 81
```bash
vim aux/ToyCovExecs/generateLvsEB2BVolCovMatrix.cc
```
AcRates_Fid.root -> AcRates_Fid_prd.root

```bash
make generateLvsEB2BVolCovMatrix
>./generateLvsEB2BVolCovMatrix test.root inputs/CovMatrices/SB2BLvsEVolCovMatrix.root 1000
```
[README](../Readme.md)
