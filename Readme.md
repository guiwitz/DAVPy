[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/guiwitz/DAVPy/master?urlpath=lab)
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/guiwitz/DAVPy/blob/master)
[![CC BY 4.0][cc-by-shield]][cc-by]

# Introduction to Data Analysis and Visualization with Python

This repository contains the course material for the course "Introduction to Data Analysis and Visualization with Python" given at Bern University by the Science IT Support unit in the frame of the [Transferable Skills](https://www.unibe.ch/research/promotion_of_early_career_researchers/ts/ts/index_eng.html) program of University of Bern's Vice-Rectorate for Development. This content has been developed by Guillaume Witz from Data Science Lab, University of Bern.

## Content

Before covering scientific programming, the course starts with an introduction to basics. This includes:
- installing and managing packages using conda
- using Jupyter notebooks for interactive programming
- using VSCode as a code editor
- using AI-coding assistants like [GitHub Copilot](https://github.com/features/copilot) or chatGPT
- Then chapters 2-8 cover the basics of Python for scientific programming. The content is not exhaustive and includes only essential data types and structures as well as flow control.

The core of the course then focuses on scientific computing and data analysis in three parts:
1. The core packages [NumPy](https://numpy.org/) and [Pandas](https://pandas.pydata.org/). These packages offer additional data structures necessary to do efficient numerical computations (NumPy arrays) and process mixed-type tabular data (Pandas dataframes).
2. Visualization. Here we show the students how arrays and dataframes can be represented as plots (scatter, histogram etc.) and how these plots can be formatted. Both the fundamental plotting library [Matplotlib](https://matplotlib.org/) as well as the higher-lever library [seaborn](https://seaborn.pydata.org/index.html) are presented.
3. Data analysis. Here we show how numerical data can in general be analysed using tools like [SciPy](https://scipy.org/) and [statsmodels](https://www.statsmodels.org/stable/install.html). We also provide a brief introduction into more specialized packages such as [scikit-learn](https://scikit-learn.org/stable/) for Machine Learning or [scikit-image](https://scikit-image.org/) for Computer Vision to provide some insight into more domain-specific problems.

## Interactive material

All the course material is offered in the form of interactive notebooks that can be executed via Jupyter (or similar software such as VSCode or Google Colab).

## Installation
### Local installation
#### Using conda
To run Python and Jupyter we strongly recommend to install the necessary software via conda. Conda is an environment manager that allows you to create for each of your projects a specific environment on your computer in which you can then install combinations of Python packages without interference between projects. Conda comes in many flavours but we strongly recommend to use Miniforge and follow the instructions on the [Miniforge website](https://github.com/conda-forge/miniforge#install). Miniforge contains a minimal version of conda and is an open-source project, ensuring that by default your packages will also come from an open-source package repository (conda-forge), avoiding potential licensing issues with Anaconda.

#### Getting the course material

You can either download or clone this GitHub repository to your computer. For download you can use the green "Code" button at the top right of this page and then unzip the downloaded folder. If you know git you can also type this is your terminal:

```
git clone https://github.com/guiwitz/DAVPy.git
```

#### Installing the environment

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

### Using Google Colab

You can open the notebooks in Colab directly by clicking on the badge at the top left of this page. Beware that you should **save a copy to your Google Drive** if you want to preserve your changes. Colab should have most software pre-installed. If one is missing you can try to install it using ```pip```.

### Using OnDemand

Jupyter is often offered as a service for example on computing clusters via OnDeman. In such as case you don't need to install Jupyter, but you will have to create a conda environment with necessary packages. This can be done by opening a terminal from the Jupyter session and running the following commands. First you need to activate conda in your session (specific to cluster usage):
```
module load Anaconda3
eval "$(conda shell.bash hook)"
```
Then create an environment. Note that packages are just given as examples but `ipykernel` is **required** here:
```
conda create -n davpy_ubelix python=3.12 numpy pandas ipykernel -c conda-forge
```
Finally, you need to activate the environment and make the kernel available in Jupyter:
```
conda activate davpy_ubelix
python -m ipykernel install --user --name davpy_ubelix
```
In the Jupyter startup page, you can then select the kernel `davpy_ubelix` to run the notebooks.


## License
This work is licensed under a [Creative Commons Attribution 4.0 International License][cc-by].

[cc-by]: http://creativecommons.org/licenses/by/4.0/
[cc-by-image]: https://i.creativecommons.org/l/by/4.0/88x31.png
[cc-by-shield]: https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg

