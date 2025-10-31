#  MLB Wins Prediction (Lahman Dataset)

**Author:** Astrid Barreras  
**Stack:** R, Quarto, Lahman, tidyverse, ggplot2, caret  
**Last Updated:** November 2024  

---

##  Project Overview

This project predicts **Major League Baseball (MLB) team wins** using historical team-level data from the **Lahman R package**.  
The workflow demonstrates a full analytics process,  from feature engineering to model evaluation,  and is designed as a reproducible **Quarto project**.

The analysis explores how variables such as **run differential**, **team offense/defense**, and **Pythagorean expectation** influence team success.

---

##  Repository Contents

| File | Description |
|------|--------------|
| `mlb-wins-prediction.qmd` | Main Quarto document. Can be rendered to HTML or PDF. Contains code, visuals, and analysis. |
| `mlb-wins-prediction.pdf` | Pre-rendered report for quick viewing (no setup required). |

---

##  How to Run the Quarto Document

1. Clone this repo
   ```bash
   git clone https://github.com/albarreras/mlb-wins.git
   cd mlb-wins
   
2. Open in RStudio (recommended) or run in terminal. Install required packages

    ```bash
    install.packages(c(
      "Lahman", "tidyverse", "janitor", "caret", "broom",
      "yardstick", "GGally", "gt", "patchwork"
    ))

3. Render the Quarto document

    ```bash
    quarto::quarto_render("mlb-wins-prediction.qmd")


This will output an .html (and optionally .pdf) report showing:

- Feature engineering

- Correlation analysis

- Linear regression model (LM)

- Cross-validation metrics (R², RMSE, MAE)

- Diagnostic plots

 Key Results
|Metric|Value|
|------|-----|
|R² (CV) |	0.95+ |
| MAE (Test)	| ~2.3 wins |
| RMSE (Test) |	~2.8 wins |

The linear regression model explains ~96% of the variance in team wins.

Run differential and Pythagorean expectation are the most predictive variables.

 Learning Goals
- Applied a complete supervised learning workflow in R.

- Used feature engineering to improve model performance.

- Interpreted model diagnostics and validation metrics.

- Demonstrated end-to-end reproducibility with Quarto.



