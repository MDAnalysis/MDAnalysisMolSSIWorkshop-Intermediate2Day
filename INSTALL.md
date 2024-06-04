# Installing the workshop environment

## Overview

This workshop is delivered mainly through a series of [Jupyter notebooks][1]
that allow for interactive Python programming. We will also be using the git version control software during this workshop. We will be using GitHub as a remote host for a git repository, which will require a GitHub account. If you do not already have one, you can create one by going to [github.com](https://github.com/), and clicking "Sign Up".


To use these, several Python packages must be installed. A full list of these
can be found in [`environment.yml`](environment.yml). 
Should you want to install MDAnalysis under a separate environment, you can find the installation instructions here: https://www.mdanalysis.org/pages/installation_quick_start/.
See below for instructions on how to set up a local copy of the Python environment.

## Installing the Python environment

Due to the complexity of the workshop environment, we strongly recommend the
use of the [Anaconda Python distribution][2]. The instructions provided here
assume the use of [conda][3].

### 1. Creating a workshop environment

To create an environment named `mda_workshop` with all the necessary
Python dependencies:

```bash
conda env create --file=environment.yml
```

See the [conda documentation][4] for more information on how to access and
manage [conda][3] environments.

To then activate this environment:

```bash
conda activate mda_workshop
```

### 2. Activating the Jupyter extensions

The workshop leverages the extended utility of several Jupyter nbextensions.

To install these, the followed should be run **once** (after having activated
the conda environment):

```bash
jupyter contrib nbextension install --user
jupyter nbextension enable splitcell/splitcell
jupyter nbextension enable rubberband/main
jupyter nbextension enable exercise2/main
jupyter nbextension enable autosavetime/main
jupyter nbextension enable collapsible_headings/main
jupyter nbextension enable codefolding/main
jupyter nbextension enable limit_output/main
jupyter nbextension enable toc2/main
```

## Installing git

With your environment activated, you can check if you have git installed with:

```bash
git --version
```

If you do not have git installed, or the version output is not at least 2.28, you should install a new version of git with:

```bash
conda install -c conda-forge git
```

Once installed, you can configure your git username and email with the following commands, inserting your name and email"

```bash
git config --global user.name "YOUR_FIRSTNAME YOUR_LASTNAME"
git config --global user.email "YOUR_EMAIL_ADDRESS"
```

## Connecting to GitHub using the Secure Shell Protocol (SSH)

Finally, you will need to setup credentials to securely push data to and retrieve data from GitHub. Follow the [instructions given by GitHub](https://docs.github.com/en/authentication/connecting-to-github-with-ssh) to create an SSH key and add it to your account.

[1]: https://jupyter-notebook.readthedocs.io/en/stable/
[2]: https://docs.anaconda.com/anaconda/install/
[3]: https://conda.io/projects/conda/en/latest/index.html
[4]: https://docs.conda.io/projects/conda/en/latest/user-guide/getting-started.html?highlight=conda%20activate#managing-environments
