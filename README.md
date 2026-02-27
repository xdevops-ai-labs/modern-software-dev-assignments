# Assignments for CS146S: The Modern Software Developer

This is the home of the assignments for [CS146S: The Modern Software Developer](https://themodernsoftware.dev), taught at Stanford University fall 2025.

## Repo Setup
These steps work with Python 3.12.

1. Install Anaconda
   - Download and install: [Anaconda Individual Edition](https://www.anaconda.com/download)
   - Open a new terminal so `conda` is on your `PATH`.

Notes: Install Miniconda instead of Anaconda.

```bash
# download and run installer
wget --no-check-certificate https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh -O miniconda_installer.sh

bash miniconda_installer.sh

# add to PATH
source ~/.bashrc

# check versions
conda --version
python --version

```

2. Create and activate a Conda environment (Python 3.12)
```bash
conda create -n cs146s python=3.12 -y
conda activate cs146s
```

3. Install Poetry
```bash
curl -sSL https://install.python-poetry.org | python -
```

Notes: Need add poetry to the path.

```bash
# add poertry to the path
export PATH="$HOME/.poetry/bin:$PATH"
echo "export PATH=\"$HOME/.poetry/bin:$PATH\"" >> ~/.bashrc
source ~/.bashrc

# check version
poetry --version
```

4. Install project dependencies with Poetry (inside the activated Conda env)
   From the repository root:
```bash
poetry install --no-interaction
```

## Repo Setup (Windows)

```powershell
# download and run installer
curl https://repo.anaconda.com/miniconda/Miniconda3-latest-Windows-x86_64.exe -o miniconda.exe
```

Double click the downloaed intaller and follow the instructions.

```powershell
# check versions
conda --version

# If conda is not recognized, initialize it:
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser -Force
& "$env:USERPROFILE\miniconda3\Scripts\conda.exe" init powershell

```

Restart ther terminal, run below commands in a new terminal.

```powershell
# accept the terms of service
conda tos accept --override-channels --channel https://repo.anaconda.com/pkgs/main
conda tos accept --override-channels --channel https://repo.anaconda.com/pkgs/r
conda tos accept --override-channels --channel https://repo.anaconda.com/pkgs/msys2

# create and activate a Conda environment (Python 3.12)
conda create -n cs146s python=3.12 -y
conda activate cs146s

# use conda to install poetry in the conda env
conda config --add channels conda-forge
conda config --set channel_priority strict

conda install -c conda-forge poetry

poetry --version

```

In the repository root:

```bash
poetry install --no-interaction
```