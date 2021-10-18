# ARM-ready machine learning packages

This repository contains pre-compiled for M1 packages. 

The idea of this repo is to have one storage for the packages and then
just include them as urls in your project's package manager.

Examples of usage of the libraries with the common package managers.

### Pipenv

```yaml
scipy = {version = "~1.8", markers = "platfotm_machine == 'x86_64'"}
scipy_m1 = {url = <github_url_to_package>, markers = "platfotm_machine == 'arm64'"}
```

### Poetry

```yaml
scipy = [
  {version = "~1.8", markers = "platfotm_machine == 'x86_64'"},
  {url = <github_url_to_package>, markers = "platfotm_machine == 'arm64'"},
]
```
