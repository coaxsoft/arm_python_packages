# ARM python packages

This repository contains pre-compiled packages for arm64. 

The idea of this repo is to have one storage for the packages (while they are not ready in their main repositories)
with the ability to include them as urls in your project's package manager.

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

## Issues & Help Wanted

## Scipy

There is an issue with `scipy`. If you install current scipy from `wheels/scipy...`
you may see an error

```shell
ImportError: dlopen(.venv/lib/python3.9/site-packages/scipy/special/_ufuncs.cpython-39-darwin.so, 2): Symbol not found: _cephes_cosdg
  Referenced from: .venv/lib/python3.9/site-packages/scipy/special/_ufuncs.cpython-39-darwin.so
  Expected in: flat namespace
 in .venv/lib/python3.9/site-packages/scipy/special/_ufuncs.cpython-39-darwin.so
```

Help wanted with resolving this problem. Read the full [issue thread regarding build](https://github.com/scipy/scipy/issues/13409)
in the Scipy repo.
