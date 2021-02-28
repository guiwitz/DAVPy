[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/guiwitz/ISDAwPython_day2/master?urlpath=lab)
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/guiwitz/ISDAwPython_day2/blob/master)

# Introduction to Statistical Data Analysis and Visualization with Python

This repository contains the course material for the second day of the course "Introduction to Statistical Data Analysis and Visualization with Python" given at Bern University by the Science IT Support unit in the frame of the [Transferable Skills](https://www.unibe.ch/forschung/nachwuchsfoerderung/ts/ts/ressource_veranstaltungen/fs21/python_fs21/python_fs21/index_ger.html#pane1014835) program of Bern University's Vice-Rectorate for Development.

## Content

After a first session covering the basics of Python and programming, this second lecture focuses on the core Python packages used for scientific computation and data science: Numpy and Pandas. Given the time-constraint, the course attempts to give an overview of essential concepts and data structures in these packages, so that participants have an entry-point in the Python scientific software stack.

## Interactive material

All the course material is offered in the form of interactive notebooks that can be executed via Jupyter or its Google equivalent Colab. As Colab doesn't require any installation, participants are expected to run their notebooks from there, and no support is provided *during* the course for local Jupyter installations. Participants who try a [local installation](#installation) and encounter problems are welcome to get in touch with the course organizers.

You can open the notebooks in Colab directly by clicking on the badge at the top left of this page. Beware that you should **save a copy to your Google Drive** if you want to preserve your changes. You can also run all notebooks in the Jupyter environment by clicking on the Binder badge. Beware that the Binder sessions are only **temporary**, so download any modification you wish to keep.

## Installation
### Using conda
To run Python and Jupyter we strongly recommend to install the necessary software via conda. Conda is an environment manager that allows you to create for each of your projects a specific environment on your computer in which you can then install combinations of Python packages without interference between projects. If you don't have conda installed, follow [these instructions](https://docs.conda.io/en/latest/miniconda.html) to install a minimal version called miniconda. You can also install [Anaconda](https://docs.anaconda.com/anaconda/install/) which on top of conda also installs a graphical interface and a long list of useful software (including non-Python software like RStudio). It takes however quite some space on disk.

### Getting the course material

You can either download or clone this GitHub repository to your computer. For download you can use the green "Code" button at the top right of this page and then unzip the downloaded folder. If you know git you can also type this is your terminal:

```
git clone https://github.com/guiwitz/ISDAwPython_day2.git
```

### Installing the environment

Now you need to create a conda environment where then you can install the necessary packages for this course. You can do this by using the provided [environment.yml](binder/environment.yml) file. If you look into it you will see that it lists a series of packages, including e.g. Numpy and Pandas, and creates an environment called ```numpypandas``` (top of the file). To create this environment, open a terminal, move to binder folder of the downloaded repository and type:

```
conda env create -f environment.yml
```

To use the environment, you then have to activate it:

```
conda activate numpypandas
```

Finally, you can start Jupyter by typing:

```
jupyter notebook
```

