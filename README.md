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

The file `spec_file.txt` contains more precise package versions and can be used to exactly reproduce the original development environment. It can only be installed on 64-bit Linux. To create an environment based `spec_file.txt`, run:
```
conda create --name <env_name> --file spec_file.txt
```
To generate a new `spec_file.txt` based on the current environment, run
```
conda list --exlicit > spec_file.txt
```

## Code Style

Format all code using [Black](https://black.readthedocs.io/en/stable/). Use a line limit of 88 characters (the default). To format a file, use the command:
```
black <FILE>
```
Black is installed in the Conda environment.
