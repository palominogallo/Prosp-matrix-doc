We must generate the PG4 toys, I have used DetectorResponse with the huber suffix. We must change the cherenkov variables like in PG4:

```bash
/output/quenching 0 BIRK2
/output/quenching 1 BIRK3
/output/cherenkov_factor CKOV
```
After running detsim and p2x, we generate like

```bash
> make generateLvsENonLinCovMatrix
> ./generateLvsENonLinCovMatrix /p/lustre2/psptexp/user/palomino/mc/covmatrix_prd/p2x_prd/   test.root  SLvsENonLinCovMat.root
```


[README](../Readme.md)
