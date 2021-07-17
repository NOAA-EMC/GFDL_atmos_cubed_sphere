Load the compiler, mpi, netCDF and FMS module

```sh
git clone -b feature/cmake_in_dycore_of_gfdl https://github.com/noaa-emc/GFDL_atmos_cubed_sphere fv3dycore_gfdl
mkdir build && cd build
cmake -DGFS_PHYS=ON ../fv3dycore_gfdl
make -j8
```
