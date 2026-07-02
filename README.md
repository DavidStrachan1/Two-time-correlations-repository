Two-time correlations repository
This repository contains Julia code and an example for calculating two-time correlation functions according to arXiv:2510.26651.
The Julia package in this repository is called CorrelationProject. The main source files are in src/, and the example notebook is in notebooks/.

The main package file is:

src/CorrelationProject.jl

which loads the source files:

include("Setup.jl")

include("map_functions.jl")


Requirements
You will need:

Julia 1.10

Git

Jupyter, VS Code, or another environment capable of running Julia notebooks



Downloading the repository:

Clone the repository with:

git clone https://github.com/DavidStrachan1/Two-time-correlations-repository.git

cd Two-time-correlations-repository

Alternatively, download the repository as a ZIP file from GitHub by selecting:

Code → Download ZIP

and then extract the folder.


One-time Julia setup:

From the repository root, start Julia with the project environment activated:

julia --project=.

Then run:

import Pkg

Pkg.instantiate()

This installs the package versions specified in Project.toml and Manifest.toml.
This setup step only needs to be run once, unless the package environment changes.



Loading the package:

After the environment has been instantiated, the package can be loaded with:

using CorrelationProject



Running the notebook:

If the notebook does not find CorrelationProject

First, check that the repository environment has been instantiated from the repository root:

cd Two-time-correlations-repository

julia --project=.

then in Julia:

import Pkg

Pkg.instantiate()

Next, check that the notebook is using a Julia kernel that respects the project environment. In Jupyter or VS Code, select the appropriate Julia kernel and restart the notebook.
I
