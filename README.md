<<<<<<< HEAD
# Two-time correlations repository

This repository contains Julia code and an example notebook for calculating two-time correlation functions according to arXiv:2510.26651.

The Julia package in this repository is called `CorrelationProject`. The main source files are in `src/`, and the example notebook is in `notebooks/`.

## Package structure

The main package file is:

```text
src/CorrelationProject.jl
```

which loads the source files:

```julia
include("Setup.jl")
include("map_functions.jl")
```

## Requirements

You will need:

- Julia 1.10
- Git
- Jupyter, VS Code, or another environment capable of running Julia notebooks

## Downloading the repository

Clone the repository with:

```bash
git clone https://github.com/DavidStrachan1/Two-time-correlations-repository.git
cd Two-time-correlations-repository
```

Alternatively, download the repository as a ZIP file from GitHub by selecting:

```text
Code → Download ZIP
```

and then extract the folder.

## One-time Julia setup

From the repository root, start Julia with the project environment activated:

```bash
julia --project=.
```

Then run:

```julia
import Pkg
Pkg.instantiate()
```

This installs the package versions specified in `Project.toml` and `Manifest.toml`.

This setup step only needs to be run once, unless the package environment changes.

## Loading the package

After the environment has been instantiated, the package can be loaded with:

```julia
using CorrelationProject
```

## If the notebook does not find `CorrelationProject`

First, check that the repository environment has been instantiated from the repository root:

```bash
cd Two-time-correlations-repository
julia --project=.
```

Then, in Julia, run:

```julia
import Pkg
Pkg.instantiate()
```

Next, check that the notebook is using a Julia kernel that respects the project environment. In Jupyter or VS Code, select the appropriate Julia kernel and restart the notebook.

If needed, install a dedicated Jupyter kernel for this repository:

```julia
import Pkg
Pkg.add("IJulia")

using IJulia

IJulia.installkernel(
    "Julia - Two-time correlations",
    "--project=/absolute/path/to/Two-time-correlations-repository"
)
```

Replace `/absolute/path/to/Two-time-correlations-repository` with the full path to the repository on your machine. Then select the kernel named `Julia - Two-time correlations` when running the notebook.

