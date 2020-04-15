## SB2BVOL

**SignalB2BVOLCovFile101**

I got the information from Danielle Berish.
I had to modify the file to have Count vs Segment in one 1D histogram. The operation only takes the error from each point

```bash
make generateLvsEB2BVolCovMatrix
>./generateLvsEB2BVolCovMatrix test.root inputs/CovMatrices/SB2BLvsEVolCovMatrix.root 1000
```
[README](../Readme.md)
