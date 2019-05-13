In the DocDB 2363 page 3, the central value is 99.929% and the sigma is 0.4%. To be conservative the sigma will be 2*0.4% (there is no assumption about correlation between parameters), and central value is hardcode to be 1, because there is correction already in MC.

```bash
>make generateLvsEB2BEScaleCovMatrix
>./generateLvsEB2BEScaleCovMatrix test.root inputs/CovMatrices/SB2BLvsEEScaleCovMatrix.root 0.007 1000
```


[README](../Readme.md)
