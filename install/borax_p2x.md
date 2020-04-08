## P2X
First we need to install libconfig

### libconfig installation

```bash
wget https://hyperrealm.github.io/libconfig/dist/libconfig-1.7.2.tar.gz
tar -xvf libconfig-1.7.2.tar.gz
mkdir libconfig-1.7.2-install
cd libconfig-1.7.2
./configure --prefix="/g/g90/palomino/Work/Prospect/Software_PRD/libconfig-1.7.2-install/"
make
make install
```

We need to include libconfig in library path before installing P2x.
My bash_profile looks like:
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

# libconfig - necessary for P2x
export LD_LIBRARY_PATH=$APP_DIR/Software_PRD/libconfig-1-7.2-install/lib/:${LD_LIBRARY_PATH}
export LDFLAGS="-L$APP_DIR/Software_PRD/libconfig-1-7.2-install/lib/ $LDFLAGS"
export CXXFLAGS="-I$APP_DIR/Software_PRD/libconfig-1.7.2-install/include/ $CXXFLAGS"
```
### P2X installatioon

```bash
git clone https://github.com/PROSPECT-collaboration/PROSPECT2x_Analysis
cd PROSPECT2x_Analysis
git checkout tags/v22.4 (I did it for 2020 prd paper)
mkdir P2x
cd P2x
cmake ../PROSPECT2x_Analysis/ -DCMAKE_PREFIX_PATH="/g/g90/palomino/Work/Prospect/Software_PRD/libconfig-1.7.2-install/"
make -j4
make install
```
Then my bash_profile will look like:
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

# libconfig - necessary for P2x
export LD_LIBRARY_PATH=$APP_DIR/Software_PRD/libconfig-1-7.2-install/lib/:${LD_LIBRARY_PATH}
export LDFLAGS="-L$APP_DIR/Software_PRD/libconfig-1-7.2-install/lib/ $LDFLAGS"
export CXXFLAGS="-I$APP_DIR/Software_PRD/libconfig-1.7.2-install/include/ $CXXFLAGS"

# P2x
export P2X_ANALYSIS_CODE=$APP_DIR/Software_Apr19/PROSPECT2x_Analysis/
export P2X_BUILD=$APP_DIR/Software_Apr19/P2x/
```

[README](../Readme.md)
