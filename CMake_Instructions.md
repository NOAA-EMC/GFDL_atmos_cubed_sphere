Load the compiler, mpi, netCDF and FMS module (2021.02.01)

```sh
git clone -b feature/cmake_in_dycore_of_gfdl https://github.com/noaa-emc/GFDL_atmos_cubed_sphere fv3dycore_gfdl
mkdir build && cd build
cmake -DGFS_PHYS=ON ../fv3dycore_gfdl
make -j8
```

The configuration will pass, but the build will fail.

[  40%] Building Fortran object CMakeFiles/fv3.dir/GFDL_tools/fv_cmip_diag.F90.o
/Users/rmahajan/scratch/ufs-tools/compile_dycore/emc-dycore/GFDL_tools/fv_cmip_diag.F90:46:5:

   46 | use atmos_cmip_diag_mod, only: register_cmip_diag_field_2d, &
      |     1
Fatal Error: Cannot open module file 'atmos_cmip_diag_mod.mod' for reading at (1): No such file or directory
compilation terminated.
