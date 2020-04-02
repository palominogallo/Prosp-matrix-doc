## SB2BESCALE

**SignalB2BESCALECovFile101**

In the DocDB 2363 page 3, the central value is 99.929% and the sigma is 0.4%. To be conservative the sigma will be 2*0.4% (We don't assume the parameters are correlated.), and central value is hardcode to be 1, because the correction is already in MC.

```bash
>make generateLvsEB2BEScaleCovMatrix
>./generateLvsEB2BEScaleCovMatrix test.root inputs/CovMatrices/SB2BLvsEEScaleCovMatrix.root 0.008 1000
```


[README](../Readme.md)
