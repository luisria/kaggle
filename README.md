# Kaggle - Competitions
## Introduction
The aim of this repository is to have a place where I could put together the work done accross different Kaggle competitions, aiming to visibilize it and be opened to criticism.
- [Requirements](#requirements)
    * [Clone Repository](#clone)
    * [Virtual Environment](#venv)
- [Code Structure](#code_struct)

## Requirements <a name="requirements"></a>
### Clone Repository <a name="clone"></a>
- Validate Git is available on your computer
    1. Open a Terminal shell
    2. Execute `git --version`
    3. In case the following message is shown: `-bash: git: command not found`, the following steps should be followed in order to download and configure Git:
        - Install [homebrew](https://brew.sh/)
        - Download Git: `brew install git`
        - Configure user name and email:
            * git config --global user.name USERNAME
            * git config--global user.email USER_EMAIL
- Clone the repository: `git clone https://github.com/luisria/kaggle.git`
### Virtual Environment <a name="venv"></a>
To be able to interact with the code without any limitation, you will require a virtual environment to be configured which can be done in different ways:
#### **Anaconda**
Having previously installed [Anaconda](https://docs.anaconda.com/free/anaconda/install/index.html), and knowing that main repository version utilises Python 3.10 as main release, we will need to run the following command within a Terminal shell in order for our environment to be available for use:
```bash
conda create --name myenv python --no-default-packages --yes python=3.10
```

To activate the virtual environment, the following command should be executed:
```bash
conda myenv activate
```

Then we will need to install poetry in order for the correct dependencies to be later on installed
```bash
pip install poetry
poetry install
```

#### **Python**
To create a new Python virtual environment we will need to run the following command:
```bash
python3.10 –m venv myenv
```

If your env is not activated, you need to activate it.
```bash
source myenv/bin/activate
```

Then we will need to install poetry in order for the correct dependencies to be later on installed
```bash
pip install poetry
poetry install
```

If the code uses a new package that is not included, please feel free to include it onto the pyproject.toml file.

## Code Structure <a name="code_struct"></a>
### kaggle
It is a Python repository which contains the following:
- **competitions**: directories containing each of the different codes per the different Kaggle competitions.
- **pyproject.toml**: main poetry configuration file.
- **utils**: Python utilities (constant setup, save/read files, graphs...)
```txt
kaggle
├── competitions
│   ├── house-prices
│       └── *.ipynb
│   ├── titanic
│       └── *.ipynb
│   ├──  . . .
│
├── pyproject.toml
└── utils
    ├── . . .
```
