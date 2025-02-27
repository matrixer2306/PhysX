# NVIDIA PhysX SDK for Linux

## Location of Binaries:

* SDK libraries: bin/linux.clang


## Required packages to generate projects:

* CMake, minimum version 3.14
* Python, minimum version 3.5
* Clang, min version 3.8
* Gcc for aarch64, min version 5.3
* curl


## Generating Makefiles:

* Makefiles are generated through a script in physx root directory: generate_projects.sh
* Script generate_projects.sh expects a preset name as a parameter, if a parameter is not provided it does list the available presets and you can select one.
* Supported presets for linux platform are: linux, linux-aarch64.
* Generated solutions are in folder compiler/linux-debug, compiler/linux-checked, compiler/linux-profile, compiler/linux-release.


## Building SDK:

* Makefiles are in compiler/linux-debug etc
* Clean solution: make clean
* Build solution: make


## PhysX GPU Acceleration:

* Requires CUDA 11.0 compatible display driver and CUDA ARCH 3.0 compatible GPU


## Required Packages for Building and Running PhysX Snippets:

* freeglut3
* libglu1
* libxdamage-dev
* libxmu6

## How to select the PhysX GPU Device:

* Set the environment variable PHYSX_GPU_DEVICE to the device ordinal on which GPU PhysX should run. Default is 0.
* Example: export PHYSX_GPU_DEVICE="1"

