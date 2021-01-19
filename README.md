# class-python-environment

Note that alternatively just use the google colab environment (Infact that is the preferred mechanism)

## Install Conda

Visit https://www.anaconda.com/products/individual


## Check your environments.

```bash
conda env list
```


Remove as needed.

```bash
conda --yes remove --name bigdata --all
```
Create and activate the new environment.


```bash
conda create --name bigdata python=3.8
conda activate bigdata
```

Add the packages into the new environment.
It is tempting [to use pip](
https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html#using-pip-in-an-environment).
It may be that some packages are not available in the main conda repositories for your platform.
In that case you may need to add additional channels.

Make sure that you execute the commands below in the specific bigdata environment created above
```bash
# conda config --prepend channels conda-forge
# ensure you are in big data environment using conda activate bigdata
conda config --set channel_priority false
conda install --yes --file requirements.txt
```

## converting between basic python and notebooks

use ipynb-py-convert

```bash
conda --yes install ipynb-py-convert
```

## Learn about Jupyter Lab

```bash
conda activate bigdata
jupyter lab
```
 Read further about https://towardsdatascience.com/jupyter-lab-evolution-of-the-jupyter-notebook-5297cacde6b
