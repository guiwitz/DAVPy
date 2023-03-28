[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/guiwitz/DAVPy/master?urlpath=lab)
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/guiwitz/DAVPy/blob/master)
[![CC BY 4.0][cc-by-shield]][cc-by]

# Introduction to Data Analysis and Visualization with Python

This repository contains the course material for the course "Introduction to Data Analysis and Visualization with Python" given at Bern University by the Science IT Support unit in the frame of the [Transferable Skills](https://www.unibe.ch/research/promotion_of_early_career_researchers/ts/ts/index_eng.html) program of University of Bern's Vice-Rectorate for Development. This content has been developed by Guillaume Witz from the Microscopy Imaging Center and Science IT Support, University of Bern.

## Content

After a first session covering the basics of Python and programming, this lecture presents how to use Python for scientific computing and data analysis in three parts:
1. The core packages [NumPy](https://numpy.org/) and [Pandas](https://pandas.pydata.org/). These packages offer additional data structures necessary to do efficient numerical computations (NumPy arrays) and process mixed-type tabular data (Pandas dataframes).
2. Visualization. Here we show the students how arrays and dataframes can be represented as plots (scatter, histogram etc.) and how these plots can be formatted. Both the fundamental plotting library [Matplotlib](https://matplotlib.org/) as well as the higher-lever library [seaborn](https://seaborn.pydata.org/index.html) are presented.
3. Data analysis. Here we show how numerical data can in general be analysed using tools like [SciPy](https://scipy.org/) and [statsmodels](https://www.statsmodels.org/stable/install.html). We also provide a brief introduction into more specialized packages such as [scikit-learn](https://scikit-learn.org/stable/) for Machine Learning or [scikit-image](https://scikit-image.org/) for Computer Vision to provide some insight into more domain-specific problems.

## Interactive material

All the course material is offered in the form of interactive notebooks that can be executed via Jupyter or its Google equivalent Colab. As Colab doesn't require any installation, participants are expected to run their notebooks from there, and no support is provided *during* the course for local Jupyter installations. Participants who try a [local installation](#installation) and encounter problems are welcome to get in touch with the course organizers.

You can open the notebooks in Colab directly by clicking on the badge at the top left of this page. Beware that you should **save a copy to your Google Drive** if you want to preserve your changes. You can also run all notebooks in the Jupyter environment by clicking on the Binder badge. Beware that the Binder sessions are only **temporary**, so download any modification you wish to keep.

## Installation
### Using conda
To run Python and Jupyter we strongly recommend to install the necessary software via conda. Conda is an environment manager that allows you to create for each of your projects a specific environment on your computer in which you can then install combinations of Python packages without interference between projects. If you don't have conda installed, follow [these instructions](https://docs.conda.io/en/latest/miniconda.html) to install a minimal version called miniconda. You can also install [Anaconda](https://docs.anaconda.com/anaconda/install/) which on top of conda also installs a graphical interface and a long list of useful software (including non-Python software like RStudio). It takes however quite some space on disk.

### Getting the course material

You can either download or clone this GitHub repository to your computer. For download you can use the green "Code" button at the top right of this page and then unzip the downloaded folder. If you know git you can also type this is your terminal:

```
git clone https://github.com/guiwitz/DAVPy.git
```

### Installing the environment

Now you need to create a conda environment where then you can install the necessary packages for this course. You can do this by using the provided [environment.yml](binder/environment.yml) file. If you look into it you will see that it lists a series of packages, including e.g. Numpy and Pandas, and creates an environment called ```DAVPy``` (top of the file). To create this environment, open a terminal, move to binder folder of the downloaded repository and type:

```
conda env create -f environment.yml
```

To use the environment, you then have to activate it:

```
conda activate DAVPy
```

Finally, you can start Jupyter by typing:

```
jupyter notebook
```

## License
This work is licensed under a [Creative Commons Attribution 4.0 International License][cc-by].

[cc-by]: http://creativecommons.org/licenses/by/4.0/
[cc-by-image]: https://i.creativecommons.org/l/by/4.0/88x31.png
[cc-by-shield]: https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg

