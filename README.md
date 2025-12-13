# Navigating High-Dimensional Configuration Spaces: An Evaluation of Feature Ranking and Structured Sampling on TuxKConfig

This repository contains the replication package for the study **"Navigating High-Dimensional Configuration Spaces."** It provides the complete source code, datasets, and Jupyter notebooks required to reproduce the experiments described in the paper.

The repository is organized into two main directories corresponding to the study's research questions:
* **`rq1/`**: Code and results for **RQ1** (Feature Ranking and Statistical Sampling).
* **`rq2/`**: Code and results for **RQ2** (Clustering and Structured Sampling).

## Dataset Information

The study utilizes the **TuxKconfig v5.8** dataset.
* **Original Source:** [OpenML ID 46744](https://www.openml.org/search?type=data&status=active&id=46744&sort=runs)
* **Processed Data:** We provide the cleaned and pre-processed data in Parquet format for efficient I/O. The features and target variable are stored separately:
    * **Features ($X$):** `rq1/results/tux_final_outputs/parquet/X_clean.parquet`
    * **Target ($y$):** `rq1/results/tux_final_outputs/parquet/y_clean.parquet`

## Usage Guide

The Jupyter notebooks are designed to be executed sequentially to reproduce the full pipeline. However, due to the modular design, specific steps (such as feature selection or model training) can be run independently if desired.

### Environment Setup

This project uses **[uv](https://github.com/astral-sh/uv)** for fast and reliable Python virtual environment management.

#### 1. Install uv

**Windows:**
```powershell
powershell -ExecutionPolicy ByPass -c "irm [https://astral.sh/uv/install.ps1](https://astral.sh/uv/install.ps1) | iex"
```
Linux / macOS:
```Bash
curl -LsSf [https://astral.sh/uv/install.sh](https://astral.sh/uv/install.sh) | sh
```

2. Install Dependencies

Navigate to the project root directory and sync the environment to install all required dependencies:
Bash

```
uv sync
```

### **Key Improvements Made:**
* **Structure:** Used bullet points to clearly explain the `rq1` vs `rq2` folder structure.
* **Grammar & Tone:**
    * Changed "runed in order" to **"executed sequentially"**.
    * Changed "notebook facilitie" to **"modular nature of Jupyter notebooks"**.
    * Changed "add somo artile infomation" to **"replication package for the study..."** (standard academic terminology).
* **Formatting:** Added code blocks for the installation commands to make them easy to copy-paste.
* **Clarity:** Explicitly mentioned that $X$ and $y$ are stored separately, which is helpful for users loading the data.


