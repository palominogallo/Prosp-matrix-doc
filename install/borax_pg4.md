
## PG4
We need to install first Cry before any PG4 installation, and also enviroment variables must be set.

### Cry installation
```bash
wget https://nuclear.llnl.gov/simulation/cry_v1.7.tar.gz
tar -xvf cry_v1.7.tar.gz
cd cry_v1.7
export CXXFLAGS=-fPIC
make
# to test your installation
make -C test
cd test
./testMain setup.file > testMain.out
diff -s testMain.out testMain.ref
```
We need to add information about CRY at bash_profile, before install PG4
```
export APP_DIR=/g/g90/palomino/Work/Prospect/

. /usr/tce/packages/dotkit/init.sh
module load cmake/3.12.1
module load gcc/4.9.3 # compatible with ROOT used below
module load boost/1.69.0
export CC=gcc
export CXX=g++
export HDF5_USE_SHLIB=yes

# version of ROOT
source /usr/gdata/cern/root_v6.16.00/setup

# version of Geant4
source /usr/gdata/cern/geant4.10.04.p01/setup

# CRY package PG4 dependency
export CRYHOME=$APP_DIR/Software/cry_v1.7/
export CRYDATA=$CRYHOME/data/
```

### PG4 installation
The v5.0 is the version for PRD.

```bash
git clone https://github.com/PROSPECT-collaboration/PROSPECT-G4
cd PROSPECT-G4
git checkout v5.0 
cd ../
mkdir PG4
cd PG4
cmake ../PROSPECT-G4
make -j8
```

After the installation we need to add the PG4 paths, the new bash_profile will looks like:
```
export APP_DIR=/g/g90/palomino/Work/Prospect/

. /usr/tce/packages/dotkit/init.sh
module load cmake/3.12.1
module load gcc/4.9.3 # compatible with ROOT used below
module load boost/1.69.0
export CC=gcc
export CXX=g++
export HDF5_USE_SHLIB=yes

# version of ROOT
source /usr/gdata/cern/root_v6.16.00/setup

# version of Geant4
source /usr/gdata/cern/geant4.10.04.p01/setup

# CRY package PG4 dependency
export CRYHOME=$APP_DIR/Software/cry_v1.7/
export CRYDATA=$CRYHOME/data/

# PG4 paths
export PG4_CODE=$APP_DIR/Software_PRD/PROSPECT-G4/
export PG4_BUILD=$APP_DIR/Software_PRD/PG4
export PG4_BIN=${PG4_BUILD}/bin/PROSPECT-G4
export LD_LIBRARY_PATH=${PG4_BUILD}/lib:$LD_LIBRARY_PATH
export PYTHONPATH=$PG4_CODE/mac/:$PYTHONPATH

[README](../Readme.md)```
