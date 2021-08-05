# Bulldozer Price Prediction

In this project, we'll use a [Bulldozer Price dataset](https://www.kaggle.com/c/bluebook-for-bulldozers/) taken from Kaggle, to create a regression machine learning model that will predict the auction price of a bulldozer, given different factors, such as different machine configurations and year of manufacturing.

Take a look at the [finished notebook](https://github.com/JorgePasco1/bulldozer-price-prediction/blob/master/bulldozer-price-regression.ipynb).

## Getting the data

You can download the full data from the link mentioned above. Or you can download this [zip](https://drive.google.com/file/d/1tFbU1bma3t6o8xAcR0_o7YRRROUhy-HG/view?usp=sharing) with the used files and the correct folder structure for the Notebook.

## Installation

First, clone this repository to your machine:

```bash
git clone https://github.com/JorgePasco1/bulldozer-price-prediction
```

### Using conda

This project uses conda as a environment/package manager. To easily run this project in your machine, you should have ananconda or miniconda installed (You might want to refer to [Conda documentation](https://docs.conda.io/en/latest/index.html)).

Then, create the environment folder with the dependencies within the project directory:

```bash
conda env create --prefix ./env -f ./environment.yml
```

Activate the environment, with:

```bash
conda activate ./env
```

And finally, if dependencies are correctly installed, you should be able to run:

```bash
jupyter notebook
```

### Troubleshooting

When creating the enviroment, you may encounter `ResolvePackageNotFound` problem:

```bash
ResolvePackageNotFound:
  - dependencies not found
```

To solve the problem, move the problematic dependecies under pip section in the .yml file, like:

```yml
dependencies:
  - appnope=0.1.0=py38_0
  - attrs=19.3.0=py_0
  - backcall=0.1.0=py38_0
  - blas=1.0=mkl
  - bleach=3.1.4=py_0
  - ca-certificates=2020.6.24=0
  - certifi=2020.6.20=py38_0
  - cycler=0.10.0=py38_0
  - dbus=1.13.14=h517e14e_0
  - decorator=4.4.2=py_0
  - defusedxml=0.6.0=py_0
  ** all dependencies, except those not found **
  - pip:
    - jedi=0.17.0=py38_0
    - jinja2=2.11.2=py_0
    - joblib=0.15.1=py_0
    - jpeg=9b=he5867d9_2
    - jsonschema=3.2.0=py38_0
    - jupyter=1.0.0=py38_7
    - jupyter_client=6.1.3=py_0
    - jupyter_console=6.1.0=py_0
    - jupyter_core=4.6.3=py38_0
    - kiwisolver=1.2.0=py38h04f5b5a_0
    - libcxx=10.0.0=1
    - libedit=3.1.20181209=hb402a30_0
    - libffi=3.3=h0a44026_1
    - libgfortran=3.0.1=h93005f0_2
    - libiconv=1.16=h1de35cc_0
    - libpng=1.6.37=ha441bb4_0
    *** All dependencies not found ***
```

### No Conda

Alternatively, you can use your preferred method to install the required dependencies (`jupyter`, `NumPy`, `Pandas`, `Matplotlib`, `scikit-learn`, `joblib` and `seaborn`); use the versions stated in the environment.yml file to reproduce the same environment used for this project.
