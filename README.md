# Programming for Data Analysis 1 (PDA1)

Course materials for **Programming for Data Analysis 1** - MBADS Program, IE University.

## Quick Start

**Open notebooks directly in Google Colab:** See [COLAB.md](COLAB.md) for one-click links to all course materials.

## Course Overview

This course provides a comprehensive introduction to Python programming with a focus on data analytics applications. Students learn fundamental Python concepts, data manipulation techniques using pandas, and practical problem-solving skills for business applications.

### Topics Covered

**Block 1: Python Fundamentals (Sessions 1-11)**
- Variables, types, and operations
- Data structures: lists, tuples, dictionaries, sets
- Strings and text processing
- Conditionals and boolean logic
- Loops and iteration
- Functions and code organization

**Block 2: Pandas for Data Analytics (Sessions 13-19)**
- Introduction to pandas and DataFrames
- Reading and writing data files
- Filtering, selecting, and aggregation
- Combining DataFrames
- Data quality and cleaning

## Repository Structure

```
pda1-mbads/
├── notebooks/     # Session notebooks
├── homework/      # Homework assignments
├── data/          # Shared datasets
├── COLAB.md       # Google Colab links
└── syllabus.md    # Full course syllabus
```

## Local Development

### Requirements
- Python >= 3.11
- pandas, numpy, plotly

### Setup with uv

```bash
# Install dependencies
uv sync

# Install dev dependencies (Jupyter)
uv sync --all-extras

# Run Jupyter
uv run jupyter notebook
```

### Setup with pip

```bash
# Create virtual environment
python -m venv .venv
source .venv/bin/activate  # On Windows: .venv\Scripts\activate

# Install dependencies
pip install pandas numpy plotly jupyter
```

## Using Google Colab

The easiest way to use these materials is through Google Colab - no local setup required!

1. Open [COLAB.md](COLAB.md)
2. Click any "Open in Colab" badge
3. Save a copy to your Drive to keep your work

Colab has pandas, numpy, and plotly pre-installed.

## License

Course materials for IE University MBADS program.
