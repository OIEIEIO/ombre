### Build for Ubuntu 16.04

Debian / Ubuntu one liner for all dependencies needed for Ubuntu 16.04  
``` sudo apt update && sudo apt install build-essential cmake pkg-config libboost-all-dev libssl-dev libzmq3-dev libunbound-dev libsodium-dev libunwind8-dev liblzma-dev libreadline6-dev libldns-dev libexpat1-dev doxygen graphviz libpgm-dev```

### Cloning the repository

Clone recursively to pull-in needed submodule(s):

`$ git clone -b oieieio https://github.com/ombre-project/ombre.git`

If you already have a repo cloned, initialize and update:

`$ cd ombre`

### Build instructions

ombre uses the CMake build system and a top-level [Makefile](Makefile) that
invokes cmake commands as needed.

#### On Ubuntu 16.04

* Install the dependencies
* Change to the root of the source code directory, change to the most recent release branch, and build:

        cd ombre
        make

    *Optional*: If your machine has several cores and enough memory, enable
    parallel build by running `make -j<number of threads>` instead of `make`. For
    this to be worthwhile, the machine should have one core and about 2GB of RAM
    available per thread.

* The resulting executables can be found in `build/release/bin`

* Run ombre with `./ombred

