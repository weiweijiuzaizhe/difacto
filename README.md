# <img src=https://raw.githubusercontent.com/dmlc/dmlc.github.io/master/img/logo-m/difacto.png width=130/> *Distributed Factorization Machines*

[![Build Status](https://travis-ci.org/dmlc/difacto.svg?branch=master)](https://travis-ci.org/dmlc/difacto)
[![codecov.io](https://codecov.io/github/dmlc/difacto/coverage.svg?branch=master)](https://codecov.io/github/dmlc/difacto?branch=master)
[![Documentation Status](https://readthedocs.org/projects/difacto/badge/?version=latest)](http://difacto.readthedocs.org/en/latest/?badge=latest)
[![GitHub license](http://dmlc.github.io/img/apache2.svg)](./LICENSE)

Fast and memory efficient library for factorization machines (FM).

- Supports both ℓ1 regularized logistic regression and factorization
  machines.
- Runs on local machine and distributed clusters.
- Scales to datasets with billions examples and features.

### Quick Start

The following commands clone and build difacto, then download a sample dataset,
and train FM with 2-dimension on it.

```bash
git clone --recursive https://github.com/dmlc/difacto
cd difacto; git submodule update --init; make -j8
./tools/download.sh gisette
build/difacto data_in=data/gisette_scale val_data=data/gisette_scale.t lr=.02 V_dim=2 V_lr=.001  batch_size=10
```

### History

Origins from
[wormhole/learn/difacto](https://github.com/dmlc/wormhole/tree/master/learn/difacto).

(NOTE: this project is still under developing)

### References

Mu Li, Ziqi Liu, Alex Smola, and Yu-Xiang Wang.
DiFacto — Distributed Factorization Machines. In WSDM, 2016
