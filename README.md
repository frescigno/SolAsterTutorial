# SolAsterTutorial

Tutorial on SolAster for the Sun-as-a-Star Workshop (Flatiron, NY)

## Setup and prerequisites

There are two main prerequisites before we can start the tutorial.

The first one is registering your email address with JSOC [here](http://jsoc.stanford.edu/ajax/register_email.html). This will allow us to download SDO images.

The second thing we need to do is to install the relevant python packages. You can use the package manager of your choice, though we recommend [`conda`](https://docs.conda.io/projects/conda/en/stable/user-guide/install/index.html) or [`poetry`](https://python-poetry.org/docs/master/).

We include instructions on how to set up a virtual envirnoment with all the packages we need below

### Conda

We provide an environment file `ENV.yml` for easy generation of a fully-populated virtual environment with `conda`:

```
conda env create --file=ENV.yml
```

If for some reason this isn't working on your device, we can manually create a virtual environment and populate it with the packages we need:

```
conda create -n SolAsterTutorial

conda install astropy jupyter matplotlib mkdocs mkdocs-jupyter mkdocs-material numpy pathlib pandas pymdown-extensi
ons python-kaleido scipy scikit-learn scikit-image sunpy notebook lxml zeep drms --yes
```

Once you have sucessfully created a virtual environment, you need to activate it so python knows which interpreter to use:

```
conda activate SolAsterTutorial
```

Once you have activated the environment, you can execute python files as normal by

```
python file.py
```

or

```
jupyter notebook
```

Finally, after the tutorial, you can return to your base environment with

```
conda deactivate
```

### Poetry

We provide a `pyproject.toml` file which lists the packages we need to run the tutorial.

To install the packages, run

```
poetry install
```

Once these packages have been installed, we tell python to use this interpreter with

```
poetry run python file.py
```

or

```
poetry run jupyter notebook
```
