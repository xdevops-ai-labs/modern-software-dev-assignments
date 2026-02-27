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