[![Documentation Status](https://readthedocs.org/projects/tslearn/badge/?version=latest)](http://tslearn.readthedocs.io/en/latest/?badge=latest)
[![Build Status](https://travis-ci.org/rtavenar/tslearn.svg?branch=master)](https://travis-ci.org/rtavenar/tslearn)
[![Code Climate](https://codeclimate.com/github/rtavenar/tslearn/badges/gpa.svg)](https://codeclimate.com/github/rtavenar/tslearn)
[![Test Coverage](https://codeclimate.com/github/rtavenar/tslearn/badges/coverage.svg)](https://codeclimate.com/github/rtavenar/tslearn/coverage)

`tslearn` is a Python package that provides machine learning tools for the analysis of time series.
This package builds on `scikit-learn`, `numpy` and `scipy` libraries.

# Dependencies

```
Cython
numpy
scipy
scikit-learn
```

# Installation

## Using PyPI

The easiest way to install `tslearn` is probably via `pip`:
```bash
pip install tslearn
```

## Using latest github-hosted version

If you want to get `tslearn`'s latest version, you can `git clone` the repository hosted at github:
```bash
git clone https://github.com/rtavenar/tslearn.git
```

Then, you should run the following command for Cython code to compile:
```bash
python setup.py build_ext --inplace
```

Also, for the whole package to run properly, its base directory should be appended to your Python path.


# Already available

* A `generators` module provides Random Walks generators
* A `preprocessing` module provides standard time series scalers
* A `metrics` module provides:
  * Dynamic Time Warping (DTW) (derived from `cydtw` code)
  * LB_Keogh
  * Global Alignment Kernel
* A domain adaptation for time series module named `adaptation` contains:
  * a method for DTW-based non linear resampling that was previously released in `dtw_resample` repo
* A `neighbors` module includes nearest neighbor algorithms to be used with time series
* A `clustering` module includes the following time series clustering algorithms:
  * Standard Euclidean k-means (with adequate array reshaping done for you)
    * Based on `tslearn.barycenters`
  * DBA k-means from Petitjean _et al._
    * Based on `tslearn.barycenters` that offers DBA facility that could be used for other applications than just 
    k-means
  * Global Alignment kernel k-means
  * KShape clustering from Paparizzos and Gravano
* A `piecewise` module includes standard time series transformations, as well as the corresponding distances:
  * Piecewise Aggregate Approximation (PAA)
  * Symbolic Aggregate approXimation (SAX)
  * 1d-Symbolic Aggregate approXimation (1d-SAX)

# TODO list

* Add soft-DTW to the proposed metrics
* Implement Learning Shapelets from Grabocka et al. (Conv+L2, + unsupervised)
* Add local feature extractors (`TransformerMixin`)
* Add soft-DTW k-means by Cuturi and Blondel
* Add metric learning for time series (Garreau _et al._)
* Add automatic retrieval of UCR/UEA datasets and 1M remote sensing time series?
* Add LB_Keogh for nearest neighbor search
* Add Itakura and SakoeChiba variants of DTW

**If you want other ML methods for time series to be added to this TODO list, do not hesitate to open an issue!**
