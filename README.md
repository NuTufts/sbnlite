# sbnlite

Translate larsoft data products into larlite format via an `art::Analyzer` module.

This module aims to be usable for SBND, ICARUS, and MicroBooNE.

## with `sbndcode`

Tested with `sbndcode` v09_64_01. Need to developing translation of `sbnd::crt::CRTdata` class.

## with `icaruscode`

Not yet tested.

## with `uboonecode`

Developed based on [ublite](https://cdcvs.fnal.gov/redmine/projects/ublite/repository).
This version not yet tested with uboonecode.

## Adding it to your code

After running `mrb newDev`, go into the `src` folder and run:

```
mrb g https://github.com/NuTufts/sbnlite
```

Note, before building, you will need to build larlite.

```
git clone https://github.com/nutufts/larlite
cd larlite
git checkout -b feature/tmw_larutil_geo_update feature/tmw_larutil_geo_update
mkdir build
cd build
cmake ../
make i -j4
```

Eventually, need the copy of larlite to be UPS product that can be loaded automatically.

## Known issues

If you get an error indicating a function is duplicated with a previous version in  `liblarcv.so`, 
deactivate `larcv` or `larcv2` that might have been autoloaded when setting up the experiment code repositories.

```
unsetup larcv2
```

Eventually, I will fix this.