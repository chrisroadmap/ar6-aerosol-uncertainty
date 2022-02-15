# ar6-aerosol-uncertainty
If we knew the distribution of aerosol forcing or ECS, how would that affect our knowledge of future projections?

## First steps
This assumes that you are developing with `conda` and `python` 3.7, 3.8 or 3.9. These instructions should work for Windows when using Anaconda Prompt and for MacOS in Terminal (and by extension, likely will work on Linux).

1. clone the repo on to your local computer
2. Create a new environment:

```
conda env create -f environment.yml
```
This will automatically make a conda environment with the required dependencies called `conditioned-projections`.

3. Then run

```
nbstripout --install
```
This will clear all output data from notebooks upon committing, making nice clean version-control friendly notebooks.

4. Examine `.gitignore` and decide where you want to put any large input or output datasets that you don't want to commit to GitHub, and fill in these paths.

## Operation

Most of the time your workflow will look like this

```
conda activate ar6-aerosol-uncertainty
jupyter notebook
```

## Updating requirements

As you build the package you will likely want to add more dependencies. Edit the `environment.yml` file and run
```
conda env update -f environment.yml --prune
```

Please do not overwrite the `environment.yml` file using `conda env export`, as this exports everything in your local environment including all sub-dependencies and OS-specific packages (and sometimes local paths).
