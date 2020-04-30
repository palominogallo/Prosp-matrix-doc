## EPeakVar

```bash
> make generateLvsEPeakVarCovMatrix
> ./generateLvsEPeakVarCovMatrix inputs/data/RxOff_2019B_16bins_10Lbins.root inputs/CovMatrices_jose/BLvsEPeakVarCovMatrix.root 0.03
```

I have to remove the nC peak in the Cov and then duplicate the unit matrix in the non diagonal elements
i used my code in notebooks EvsPeak
