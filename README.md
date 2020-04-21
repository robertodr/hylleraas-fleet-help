# The Hylleraas fleet
In December 2019 the centre acquired 2 new machines. The machines were obtained with the idea of having local resources with immediate availability for debuggin and testing on high-end hardware.
## The machines

Both machines are running [Debian 10](https://www.debian.org).

`woolf` (named after [Virginia Woolf](https://en.wikipedia.org/wiki/Virginia_Woolf)) is an Intel machine:
- Intel [Xeon W2295](https://ark.intel.com/content/www/us/en/ark/products/198011/intel-xeon-w-2295-processor-24-75m-cache-3-00-ghz.html) CPU
- 128 GB of DDR4 2666 MHz RAM
- Nvidia [Quadro RTX4000](https://www.nvidia.com/en-us/design-visualization/quadro/rtx-4000/) GPU
- 1 TB SSD (`/scratch` partition)
- 10 TB HDD

`sandel` (named after [Cora Sandel](https://no.wikipedia.org/wiki/Cora_Sandel)) is an AMD machine:
- AMD [Ryzen Threadripper 2990WX](https://www.amd.com/en/products/cpu/amd-ryzen-threadripper-2990wx) CPU
- 64 GB of DDR4 2933 MHz RAM
- Nvidia [Quadro RTX4000](https://www.nvidia.com/en-us/design-visualization/quadro/rtx-4000/) GPU
- 1 TB SSD (`/scratch` partition)
- 6 TB HDD

## Installed packages
### The AOCC compiler
The [AMD optimizing compiler (AOCC)](https://developer.amd.com/amd-aocc/) is an optimizing frontend to the Clang family of compilers tailored for AMD CPUs. Do the following to use AOCC in `sandel`
 ```
 $ source /opt/AMD/aocc-compiler-2.1.0/setenv_AOCC.sh
 ```
The compiler will be available as `clang` for C, `clang++` for C++, and `flang` for Fortran.

### Intel MKL
The latest version (2020.0-088) of the [Intel Math Kernel Libraries](https://software.intel.com/en-us/mkl) is globally installed. However, the libraries are not _globally_ on `PATH` or `LD_LIBRARY_PATH`. To do so, run:
```
source /opt/intel/compilers_and_libraries_2020/linux/mkl/bin/mklvars.sh intel64
```

### Intel MPI
The latest version (2019.6-088) of the [Intel MPI](https://software.intel.com/en-us/mpi-library) is globally installed. Note that the installed version provides wrappers for the GCC family of compilers. The compiler wrappers are not _globally_ on `PATH`. To do so, run:
```
source /opt/intel/compilers_and_libraries_2020/linux/mpi/intel64/bin/mpivars.sh intel64
```

If you plan to use **both** Intel MKL and Intel MPI it is enough to just run the following:
```
source /opt/intel/bin/compilervars.sh intel64
```

**NOTE** `sandel` is an AMD machine and the Intel products might not offere full support for the CPU.

## GPU programming

## Docker and Singularity
You can build and run images and containers with both [Docker](https://docs.docker.com/install/) and [Singularity](https://sylabs.io/). All users are part of the `docker` group and thus can use Docker without superuser privileges.

## Package managers
### `pip`+`virtualenv`, Pipenv, and poetry
### Nix
### Conda
### Spack

## Jupyter notebook
1. `ssh` into your favorite author.
2. Install jupyter notebook using your favorite package manager.
3. On Sandel/woolf run `jupyter notebook --no-browser --port xxxx`.
4. Locally run `ssh -NL xxxx:localhost:xxxx <username>@<favorite author>.chem.uit.no`.
5. Open your web-browser locally and copy paste the link generated when you did step 3.

xxxx is some 4 digit number eg., 1234. Pick your favorite, if one does not work move on
to your second favorite 4 digit number.

## Getting an account
In order to obtain an account, we ask you to fill this [Google form](https://docs.google.com/forms/d/e/1FAIpQLSc6PJvJRLYuoJs_PdA0GNmKgFBLkUyVdez2LoeJtVtd5wNhog/viewform?usp=sf_link) with your contact information and desired username. You will be contacted with further instructions.
