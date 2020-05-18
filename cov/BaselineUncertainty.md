## SBLSHIFT

Inside src/TExperiment.cc
uncomment the line with **gen_cov_baseline**, that prints on screen some information to be saved on txt file

```bash
> #define gen_cov_baseline 
```

An option how to create this cov mat
```bash
> cd OscSens_CovMatrix 
> make
> make generateSetupFiles
> mkdir temp
> mkdir temp/mac
> cd temp
> cp ../aux/prepareCovMatBaseline.py .
> cp ../mac/covmatBaseL.mac mac/.
> python prepareCovMatBaseline.py
```


Generate the reference setup file to be used as reference and 1000 files with the origin deviated randomly. It will produce the output *Set.root* and others.
You can create scripts to run those files as:

```bash
> tail run1.sh
./generateSetupFiles 2> temp/out
for i in `seq 0 199`;
do
        ./generateSetupFiles temp/mac/default$i.mac 2> temp/out$i
done
```
Could be run the scripts like:
```bash
> source run1.sh
```

```bash
> cp aux/cleanForCovMatBaseline.C
> root cleanForCovMatBaseline.C
```

```bash
> make generateLvsEBaselineCovMatrix
> ./generateLvsEBaselineCovMatrix  /p/lustre2/psptexp/user/palomino/OscSens_CovMatrix/rootfiles/  /p/lustre2/psptexp/user/palomino/OscSens_CovMatrix/rootfiles/out.root  SLvsEBaselineCovMatrix.root
```
[README](../Readme.md)
