# AIFeynman Project Setup Guide

## Installation

The first step is to install the AIFeynman library on your computer. AIFeynman supports Linux or MacOS systems. Follow these steps to set up the project:

1. **Build a virtual environment:**

    ```bash
    pip install virtualenv
    virtualenv -p python3 feyn
    source feyn/bin/activate
    ```

2. **Installing the required compiler "gfortran":**

    ```bash
    sudo apt-get update
    sudo apt-get install gfortran
    ```

    Open the `~/.bashrc` file.

    ```bash
    nano ~/.bashrc
    ```

    Add the following lines to your `~/.bashrc` file to set environment variables:

    ```bash
    export FC=gfortran
    export F77=gfortran
    ```

    Press Control+X to exit, press Y to save, and press Enter to exit.

    Run the following code to refresh the settings:

    ```bash
    source ~/.bashrc
    ```

3. **Installing the required library "numpy" and ipykernel:**

    ```bash
    pip install numpy
    pip install ipykernel
    python -m ipykernel install --user --name=feyn
    ```

4. **Installing the AIFeynman library:**

    It is better to have a Python version before 3.12.

    ```bash
    pip install aifeynman
    ```

5. **Opening Jupyter Notebook to build a Python file:**

    ```bash
    jupyter notebook
    ```

    After entering Jupyter Notebook, when choosing the new file's type, create a file of type "feyn". The installation steps are finished.
