## Conda Environment

To create the Conda environment, run:
```
conda env create --file environment.yml
```
Then activate the environment with:
```
conda activate <env_name>
```

To update the environment after modifying `environment.yml`, run the following (after activation):
```
conda env update --file environment.yml --prune
```

The file `environment_precise.yml` contains more exact package versions and can be used to reproduce the original development environment. To create an environment based on `environment_precise.yml`, run:
```
conda env create --file environment_precise.yml
```
To generate a new `environment_precise.yml` based on the current environment, run
```
conda env export > environment_precise.yml
```

## Code Style

Format all code using [Black](https://black.readthedocs.io/en/stable/). Use a line limit of 88 characters (the default) for both code and docstrings/comments. To format a file, use the command:
```
black <FILE>
```
Black is installed in the Conda environment.
