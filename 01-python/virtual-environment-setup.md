# Year 1 Python Virtual Environment & Data Science Stack Setup

Setting up an isolated Python virtual environment ensures your `algorithm-practice` repository remains clean, reproducible, and free from global package conflicts.

---

## Step 1: Create and Activate the Virtual Environment

Open your terminal (WSL, macOS, or Command Line) and navigate to your main repository root:

```bash
# Navigate to your repository
cd algorithm-practice

# Create a virtual environment named .venv
python -m venv .venv
```

Activate the environment based on your operating system:

- **Linux / WSL / macOS:**
  ```bash
  source .venv/bin/activate
  ```
- **Windows (Command Prompt):**
  ```cmd
  .venv\Scripts\activate.bat
  ```
- **Windows (PowerShell):**
  ```powershell
  .venv\Scripts\Activate.ps1
  ```

> **Note:** Once activated, your terminal prompt will display `(.venv)` at the beginning of the line.

---

## Step 2: Upgrade Core Package Utilities

Before installing your dependencies, ensure `pip`, `setuptools`, and `wheel` are up to date:

```bash
python -m pip install --upgrade pip setuptools wheel
```

---

## Step 3: Configure `requirements.txt`

Create or update your `requirements.txt` file in the repository root with the essential Year 1 data science stack:

```text
# Data Wrangling & Manipulation
pandas>=2.2.0
polars>=0.20.0
numpy>=1.26.0

# Visualization
matplotlib>=3.8.0
seaborn>=0.13.0
plotly>=5.18.0

# Scientific & Interactive Development
scipy>=1.12.0
jupyterlab>=4.1.0
notebook>=7.1.0

# Code Quality & Utilities
black>=24.0.0
ipywidgets>=8.1.0
```

---

## Step 4: Install Dependencies & Verify

Run `pip` to install all declared packages:

```bash
pip install -r requirements.txt
```

Verify the installation by running an inline check script:

```bash
python -c "import pandas as pd, polars as pl, matplotlib as plt, numpy as np; print('All core libraries imported successfully!')"
```

---

## Step 5: Configure `.gitignore` and Commit to Git

Ensure `.venv` is listed in your `.gitignore` file to avoid pushing environment files to GitHub:

```text
# Python virtual environment
.venv/
env/

# Python cache & build artifacts
__pycache__/
*.py[cod]

# Data files (keep raw files local)
data/*.csv
data/*.parquet
```

Commit your configuration files to GitHub:

```bash
# Stage changes
git add requirements.txt .gitignore

# Commit changes
git commit -m "chore: configure Year 1 Python dependencies and environment tracking"

# Push to remote main branch
git push origin main
```

---

## Quick Reference Summary

| Action | Command |
| :--- | :--- |
| **Activate (Linux/macOS/WSL)** | `source .venv/bin/activate` |
| **Activate (Windows PS)** | `.venv\Scripts\Activate.ps1` |
| **Deactivate Environment** | `deactivate` |
| **Install Requirements** | `pip install -r requirements.txt` |
| **Update Requirements** | `pip freeze > requirements.txt` |
