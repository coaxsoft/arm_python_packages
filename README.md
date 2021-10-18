# ARM python packages

This repository contains pre-compiled packages for arm64. 

The idea of this repo is to have one storage for the packages (while they are not ready in their main repositories)
with the ability to include them as urls in your project's package manager.

Examples of usage of the libraries with the common package managers.

## Install scikit-learn on M1

### Installation with Pipenv

1. Look for required scipy in [Anaconda's pypi](https://pypi.anaconda.org/scipy-wheels-nightly/simple/scipy/)
2. Download `scipy` from [Anaconda's pypi](https://pypi.anaconda.org/scipy-wheels-nightly/simple/scipy/)
3. Download scikit-learn from this repository
4. Place them at `.wheels` directory of your project
5. Edit your `Pipfile` to have these lines included

```yaml
scipy = {versions = "*", markers = "platfotm_machine != 'arm64'"}
scipy-m1 = {path = ".wheels/scipy-1.8.0.dev0+1753.a063cf3-cp38-cp38-macosx_11_0_arm64.whl", markers = "platfotm_machine == 'arm64'"}

scikit-learn = {versions = "*", markers = "platfotm_machine != 'arm64'"}
scikit-learn-m1 = {path = ".wheels/scikit_learn-1.1.dev0-cp39-cp39-macosx_11_0_universal2.whl", markers = "platfotm_machine == 'arm64'"}
```

5. Run `pipenv install --skip-lock && pipenv lock --pre`

Please, feel free to reach us out if you find more elegant way of doing the installation.

## Issues & Help Wanted

## Scipy

Scipy is not arm64-ready now. Read more about the status of Scipy in
[issue comment 1](https://github.com/scipy/scipy/issues/13409#issuecomment-902761019).

:white_check_mark: What actually works is the pre-build from anaconda. [Read here](https://github.com/scipy/scipy/issues/13409#issuecomment-904548388).

