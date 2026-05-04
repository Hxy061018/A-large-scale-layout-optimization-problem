# Dumplings Optimization: Operations Research Project

This repository contains the Group 7 final project for an Operations Research course. The project builds a mathematical optimization framework for dumpling food-truck deployment and customer assignment, with the goal of maximizing daily profit under operational constraints.

## Team

School of Management, Harbin Institute of Technology

Team members: Xiaoyu Hu, Haoyu Yang, Jingyi Hou, Chenting Lin, Ziao Gao, Xihe Jiang, Bohan Zhang

## Repository Structure

```text
.
|-- model.ipynb          # Data generation, base model, scalability tests, and figures
|-- dual_anal.ipynb      # LP relaxation, dual variables, and complementary slackness
|-- sens_anal.ipynb      # Sensitivity analysis and network visualizations
|-- business.ipynb       # Business insights and profit contribution charts
|-- datas/               # CSV datasets and generated model outputs
|-- reports/
|   |-- report.md        # Markdown version of the final report
|   `-- report.pdf       # PDF version of the final report
|-- requirements.txt     # Python dependencies
`-- .gitignore
```

## Setup

Create a virtual environment and install the dependencies:

```bash
python -m venv .venv
.venv\Scripts\activate
pip install -r requirements.txt
```

On macOS or Linux, activate the environment with:

```bash
source .venv/bin/activate
```

## Reproduce the Results

Run the notebooks from the repository root in this order:

1. `model.ipynb`
2. `dual_anal.ipynb`
3. `sens_anal.ipynb`
4. `business.ipynb`

The notebooks read from and write to the `datas/` directory. Running them from the repository root keeps the relative paths consistent.

## Solver Note

Most linear programming models can be solved with PuLP and its default CBC solver. Some advanced scalability experiments use `gurobipy`, which requires a valid Gurobi license.

## Data Files

The `datas/` directory includes:

- `advanced_model_7day_demand.csv`
- `advanced_10_cust_strict_comparison.csv`
- `basic_lp_binding_constraints.csv`
- `basic_lp_fractional_vars.csv`
- `basic_lp_summary_comparison.csv`
- `scalability_alpha_matrix.csv`
- `scalability_customer_data.csv`
- `scalability_location_coords.csv`
