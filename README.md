# Programming_for_datasci
# Programming for Data Science

A Python project for learning and practicing data science using **uv**, **Pandas**, **Seaborn**, **Matplotlib**, and **Jupyter**.

## Project Setup

This project uses [`uv`](https://docs.astral.sh/uv/) as the Python package and project manager.

### 1. Install `uv`

Install `uv` using `pip`:

```bash
pip install uv
```

Verify the installation:

```bash
uv --version
```

### 2. Initialize the Project

From the project directory:

```bash
uv init
```

This creates the Python project configuration, including `pyproject.toml`.

The project is named:

```text
programming-for-datasci
```

### 3. Check Python Version

Check the installed Python version:

```bash
python --version
```

This project currently uses Python 3.14.

> **Note:** `uv init` configured the project with a Python requirement of `>=3.14`. Therefore, creating a virtual environment with Python 3.11 produces a compatibility warning.

### 4. Create the Virtual Environment

Create a virtual environment using Python 3.14:

```bash
uv venv --python 3.14
```

Activate it:

```bash
source .venv/bin/activate
```

After activation, your terminal should show something similar to:

```text
(Programming_for_datasci)
```

### 5. Upgrade `pip`

Use:

```bash
python3 -m pip install --upgrade pip
```

Make sure to type `--upgrade` correctly.

The following commands are incorrect:

```bash
python3 -m pip install --upgade pip
python3-m pip install--upgrade pip
```

The first contains a spelling mistake, while the second is missing spaces.

## Install Data Science Packages

### Pandas

Install Pandas with:

```bash
uv add pandas
```

This also installs its required dependencies, such as NumPy.

### Seaborn and Matplotlib

Install visualization libraries:

```bash
uv add seaborn matplotlib
```

These packages are used for data visualization and exploratory data analysis.

### Jupyter

Install Jupyter:

```bash
uv add jupyter
```

This provides the tools needed to work with Jupyter notebooks.

## Project Structure

The project currently follows this structure:

```text
Programming_for_datasci/
│
├── .venv/
├── data/
│
├── L1/
│   └── L1.ipynb
│
├── pyproject.toml
├── uv.lock
└── README.md
```

### Directories and Files

| Item             | Purpose                           |
| ---------------- | --------------------------------- |
| `.venv/`         | Python virtual environment        |
| `data/`          | Storage for datasets              |
| `L1/`            | Lesson 1/coursework               |
| `L1/L1.ipynb`    | Lesson 1 Jupyter notebook         |
| `pyproject.toml` | Project metadata and dependencies |
| `uv.lock`        | Locked dependency versions        |
| `README.md`      | Project documentation             |

## Working with Jupyter

After activating the virtual environment, start Jupyter with:

```bash
uv run jupyter lab
```

Alternatively:

```bash
jupyter lab
```

You can then open:

```text
L1/L1.ipynb
```

for the first lesson.

## Useful `uv` Commands

### View available commands

```bash
uv
```

### Add a package

```bash
uv add package-name
```

Example:

```bash
uv add pandas
```

### Remove a package

```bash
uv remove package-name
```

### Synchronize dependencies

```bash
uv sync
```

### View installed dependency tree

```bash
uv tree
```

### Create a virtual environment

```bash
uv venv
```

### Run a command inside the project environment

```bash
uv run python
```

For Jupyter:

```bash
uv run jupyter lab
```

## Common Mistakes

### Activating the virtual environment

Incorrect:

```bash
source.venv/bin/activate
```

Correct:

```bash
source .venv/bin/activate
```

There must be a space between `source` and `.venv`.

### Moving to the Parent Directory

Incorrect:

```bash
cd . .
```

Correct:

```bash
cd ..
```

`..` represents the parent directory.

### Upgrading pip

Incorrect:

```bash
python3 -m pip install --upgade pip
```

Correct:

```bash
python3 -m pip install --upgrade pip
```

### Python Version Compatibility

If the project requires Python `>=3.14`, avoid creating the environment with Python 3.11:

```bash
uv venv --python 3.11
```

Instead, use:

```bash
uv venv --python 3.14
```

## Installed Dependencies

The main data science dependencies are:

* **Pandas** — data manipulation and analysis
* **NumPy** — numerical computing
* **Matplotlib** — data visualization
* **Seaborn** — statistical data visualization
* **Jupyter** — interactive notebooks

The exact dependency versions are managed by `uv.lock`.

## Recommended Workflow

For future lessons, the general workflow is:

```bash
# Activate the environment
source .venv/bin/activate

# Add a required package
uv add package-name

# Start Jupyter
uv run jupyter lab
```

For example:

```bash
source .venv/bin/activate
uv add pandas matplotlib seaborn
uv run jupyter lab
```

## Project Goal

The goal of this project is to develop practical Python and data science skills through hands-on exercises, including:

* Python programming
* Data manipulation
* Data cleaning
* Exploratory data analysis
* Data visualization
* Statistical analysis
* Jupyter Notebook workflows

---

**Project:** Programming for Data Science
**Package Manager:** uv
**Primary Language:** Python
**Environment:** Python 3.14+
