# ARM python packages

This repository contains pre-compiled packages for arm64. 

The idea of this repo is to have one storage for the packages (while they are not ready in their main repositories)
with the ability to include them as urls in your project's package manager.

`scikit-learn` now has native support of ARM :white_check_mark:

## Comments on packages

### XGBoost

There is pre-built `xgboost==1.6.0dev` package wheel. But you can build it yourself, version `1.5.0rc1`
can be installed on M1. [Read more here](https://github.com/dmlc/xgboost/issues/7260).

Ensure that you have `cmake` installed.

1. `brew install cmake`
2. `pip install xgboost==1.5.0rc1`

### Torchtext

While `pytorch` has native support of ARM, their subpackage `torchtext` is not.

There is pre-build wheel but you can build it yourself following torchtext's build [instructions](https://github.com/pytorch/text#building-from-source).
