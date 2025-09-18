
# Conda Commands Guide

## List environments
```bash
conda env list
```

## Update conda and upgrade all packages
```bash
conda update -n base conda
conda update -n PROJECT_ENV conda
conda update -n PROJECT_ENV --all
```

## Update pip3 and upgrade all packages
```bash
conda activate PROJECT_ENV
pip3 install --upgrade pip       
pip-review --local --interactive -a
```
**Note** in case of warning that not all dependencies are taken into account, rerun pip-review (last code line)

## Purge pip cache
In case of issue with a particular dependendency (e.g supabase/supafunc)
```bash
pip3 uninstall my_package
pip3 cache purge
pip3 install --force-reinstall my_package
```
