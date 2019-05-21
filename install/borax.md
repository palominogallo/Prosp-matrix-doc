## Installation on Borax
These steps worked in May 2019
```bash
ssh -Y palomino@borax.llnl.gov
```
Password must be your 8 character passphrase followed immediately by your 6 character RSA fob code.

```bash
mkdir -p Work/Prospect/Software_PRD
vim .bash_profile
```
This is the view on my bash_profile file before start doing any installation, this one was based on [Prospect wiki link](https://wiki.wlab.yale.edu/prospect/Instructions%20for%20compiling%20P2x%20on%20borax)
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
```
## PG4
[PG4 installation](install/borax_pg4.md)

## P2X
[P2X installation](install/borax_p2x.md)

