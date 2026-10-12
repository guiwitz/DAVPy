[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/guiwitz/DAVPy/blob/master)
[![CC BY 4.0][cc-by-shield]][cc-by]

# Introduction to Data Analysis and Visualization with Python

This repository contains the course material for the course "Introduction to Data Analysis and Visualization with Python" developed by Guillaume Witz at the Data Science Lab, University of Bern. It is intended for students and researchers who want to gain practical skills in data analysis and visualization using Python and have **no previous experience** in Python programming. The course is not meant to provide an exhaustive overview of Python programming but rather to equip learners with the essential skills needed for data analysis and visualization tasks.

## Content

The current repository only covers the coding part of the course. In typical live training sessions, the first part of the course is dedicated to "tooling" i.e. how and where to write and run Python code and typically covers:

- installing and managing packages (e.g., conda, pixi)
- using Jupyter notebooks for interactive programming
- using VSCode as a code editor
- using AI-coding assistants like [GitHub Copilot](https://github.com/features/copilot) or chatGPT

Chapters 2-8 cover the basics of Python for scientific programming. The content is not exhaustive and includes only essential data types and structures as well as flow control.

The core of the course then focuses on scientific computing and data analysis in three parts:
- An introduction to handling [NumPy](https://numpy.org/) arrays, the fundamental data structure for numerical computations in Python. Here again the course cannot be exhaustive but covers most aspects beginners are likely to encounter: array creation, mathematical operations on arrays, slicing and indexing.
- An introduction to [Pandas](https://pandas.pydata.org/) DataFrames, the fundamental data strcuture to handle tabular data, which serves also as "data-store" in many other packages such as scikit-learn. Here we cover DataFrame creation, simple mathematical operations on DataFrames, database-like operations such as joins, extraction and summariztion of content such as grouping indexing etc.
- An introduction to data plotting. Here we use [seaborn](https://seaborn.pydata.org/index.html), a plotting library 1. offering a wide choice of plot types, 2. using a simple and coherent API, and 3. creating plots with good defaults. As seaborn builds on top of the powerful but more complex to use librry [Matplotlib](https://matplotlib.org/), we also give an introdcution to the key concepts of the latter library.

A set of supplementary notebooks gives an overview of more advanced analysis libraries including:
 - [scikit-learn](https://scikit-learn.org/stable/) for Machine Learning
 - [statsmodels](https://www.statsmodels.org/stable/install.html) for statistical models. Participants are encouraged to look through them to get an insight into more specialized tools and techniques beyond the core course content.
 - [SciPy](https://scipy.org/) for generic scientific computing tasks
 - [scikit-image](https://scikit-image.org/) for image processing tasks

## Interactive material

All the course material is offered in the form of interactive notebooks that can be executed via Jupyter (or similar software such as VSCode or Google Colab).

## Installation
### Local installation
To run Python and Jupyter we strongly recommend to install the necessary software via conda or pixi. These two software are environment managers that allow you to create for each of your projects a specific environment on your computer in which you can then install combinations of Python packages without interference between projects. Conda comes in many flavours but we strongly recommend to use Miniforge and follow the instructions on the [Miniforge website](https://github.com/conda-forge/miniforge#install). Miniforge contains a minimal version of conda and is an open-source project, ensuring that by default your packages will also come from an open-source package repository (conda-forge), avoiding potential licensing issues with Anaconda. [Pixi](https://pixi.prefix.dev/latest/) is a newer environment manager that is also open-source and can be used as an alternative to conda. In particular it allows for a simpler tracking of dependencies, especially across conda and pypi.

To simplify the creation of the environment we provide files that contain descriptions of the necessary packages and their versions for both conda and pixi. So in the first step, you need to get access to those files. This can be done by either downloading or cloning this GitHub repository to your computer. For download you can use the green "Code" button at the top right of this page and then unzip the downloaded folder. If you know git you can also type this is your terminal:

```
git clone https://github.com/guiwitz/DAVPy.git
```

Now you need to create a conda environment where then you can install the necessary packages for this course. You can do this by using the provided [environment.yml](environment.yml) file for conda or [pixi.toml](pixi.toml) file for pixi. If you look into those files you will see that they lists a series of packages, including e.g. Numpy and Pandas. To create this environment, open a terminal and move to the main folder of the downloaded repository. Then for pixi you can type:

```
pixi install
```

To then run Jupyter you can type:

```
pixi run jupyter lab
```

For conda you can type:

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

Jupyter is often offered as a service for example on computing clusters via OnDemand. In such as case you don't need to install Jupyter, but you will have to create a conda environment with necessary packages. This can be done by opening a terminal from the Jupyter session and running the following commands. First you need to activate conda in your session (specific to cluster usage):

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

