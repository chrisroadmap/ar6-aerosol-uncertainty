# ar6-aerosol-uncertainty
If we could reduce the uncertainty in either aerosol radiative forcing or equilibrium climate sensitivity (ECS), how would that affect our knowledge of future projections?

## First steps
This assumes that you are using `conda` and `python` 3.6, 3.7, 3.8, 3.9 or 3.10. These instructions should work for Windows when using Anaconda Prompt and for MacOS in Terminal (and by extension, likely will work on Linux).

There are two options depending on whether you just want to reproduce the results and possible make your own changes locally, without pushing anything back to the main repository, or whether you intend to make code changes.

### To reproduce
1. clone the repo on to your local computer
2. Create a new environment:

```
conda env create -f environment.yml
```
This will automatically make a conda environment with the required dependencies called `ar6-aerosol-uncertainty`.

N.B. if you want to call it anything else, edit the first line of the `environment.yml` file.

3. Activate environment

```
conda activate ar6-aerosol-uncertainty
```

4. Start a notebook server

```
jupyter notebook
```

5. Run the notebooks in order.

### To develop

1. Fork the repository to your own GitHub account.
2. Clone
3. Create environment
4. Run

```
nbstripout --install
```
This will clear all output data from notebooks upon committing, making nice clean version-control friendly notebooks.

5. Examine `.gitignore` and decide where you want to put any large input or output datasets that you don't want to commit to GitHub, and fill in these paths.
6. Do development work
7. Create a pull request from your fork to the original repo.

If you need to add more packages, edit the `environment.yml` file and run
```
conda env update -f environment.yml --prune
```
