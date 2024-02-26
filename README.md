# fastplotlib-scipy2024

All materials for the `pygfx` and `fastplotlib` SciPy 2024 Tutorial.

## Installation

We will be using a JupyterHub that's been set up for this tutorial. If you would like to run the tutorial locally you may use the instructions below. We recommend testing your installation before the start of the tutorial :) .

### PyPi Install

Install using `pip`.

We will be using JupyterLab for the duration of the tutorial.

```commandline
pip install "fastplotlib[notebook]"
```

This will install everything necessary for `fastplotlib` and `pygfx` needed for the tutorial.

**Recommended: install simplejpeg for much faster notebook visualization, this requires you to first install [libjpeg-turbo](https://libjpeg-turbo.org/)**

```commandline
pip install simplejpeg
```
### Dev Install

Get `wgpu-py`, `pygfx`, and `fastplotlib` from GitHub. 

Install `wgpu-py`
```commandline
git clone https://github.com/pygfx/wgpu-py.git
cd wgpu-py

# install dev requirements
pip install -r dev-requirements.txt
# install in editable mode
pip install -e .

# get the upstream wgpu-native binaries
python download-wgpu-native.py
```

Install `pygfx`
```
# install pygfx 
git clone https://github.com/pygfx/pygfx.git
cd pygfx

# if you use a venv, create and activate it
pip install -e .[dev,docs,examples]
```
> **NOTE**
> `fastplotlib` uses [git-lfs](https://git-lfs.com/) for storing large files, so you will need to [install it](https://github.com/git-lfs/git-lfs#installing) before cloning the repo.

Install `fastplotlib`
```
git clone https://github.com/fastplotlib/fastplotlib.git
cd fastplotlib

# install all extras in place
pip install -e ".[notebook,docs,tests]"
```
> If you cloned before installing `git-lfs`, you can run `git lfs pull` at any time to properly download files.
