# Urban Morphology with Python: City Structure as Predictor and Target

The materials for the GISRUK 2025 on Urban Morphology with Python.

## Setting up to follow the workshop

### Step 1: Download the workshop material

If you are a git user, you can get the workshop materials by cloning this repo:

```sh
git clone https://github.com/martinfleis/gisruk2025.git
cd gisruk2025
```

Otherwise, to download the repository to your local machine as a zip-file,
click the `download ZIP` on the repository page
<https://github.com/martinfleis/gisruk2025>
(green button "Code"). After the download, unzip on the location you prefer
within your user account (e.g. `My Documents`, not `C:\`).

### Step 2: Install the required Python packages

You can set the environment to run the notebook in a few ways - Pixi (recommended), Conda/Mamba, uv / pip.

#### Pixi

If you'd like to run the notebook, you can create an environment using [Pixi](https://pixi.sh/latest/). See the Pixi [installation instructions](https://pixi.sh/latest/#__tabbed_1_2).

With Pixi installed, clone the repository, open a command line, and start Jupyter Lab from the included Pixi environment. Pixi will automatically install all required dependencies and start the Jupyter Lab IDE with the notebook.

```sh
pixi run jupyter lab workshop.ipynb
```

#### Conda/Mamba

If you prefer to use conda-based solutions (conda, mamba, anaconda, micromamba), you can create a conda environment using attached environment.yml file.

Using conda, we recommend to create a new environment with all packages using
the following commands (after cloning or downloading this GitHub repo and
navigating to the directory, see above):

```bash
# setting the configuation so all packages come from the conda-forge channel
conda config --add channels conda-forge
conda config --set channel_priority strict
# mamba provides a faster implementation of conda
conda install mamba
# creating the environment
mamba env create --file environment.yml
# activating the environment
conda activate gisruk2025
```

Then you can start the notebook.

```sh
jupyter lab workshop.ipynb
```

#### MyBinder

In case you do not want to install everything and just want to try out the course material, use the environment setup by Binder [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/martinfleis/gisruk2025/main?urlpath=lab/) and open the notebook right away. Note that the performance may not be optimal.

#### uv / pip / Google Colab

You can also install the necessary dependencies from PyPI using `pip`. The instructions can be used both locally and within Google Colab. With `uv`, just prepend `pip` commands with `uv` to get `uv pip ...`.

```bash
pip install momepy scikit-learn numba osmnx geopy matplotlib mapclassify folium clustergram bokeh geoplanar neatnet
```

If you are working locally (not using Google Colab), you may want to install Jupyter Lab as well.

```bash
pip install jupyterlab
```

Then you can start the notebook.

```sh
jupyter lab workshop.ipynb
```