## Meta-Analysis of LLMs and Persuasion

This repository contains the code, data, and analysis for a meta-analysis investigating the persuasive effectiveness of Large Language Models (LLMs) compared to human communicators.

## Repository Structure

- `Code/` – Main analysis in `Meta_Analysis_Markdown.Rmd` (R Markdown file that produces both HTML and PDF reports)
- `Data/` – Input data for the meta-analysis (currently `Data_final.xlsx`)
- `Plots/` – Generated outputs: forest plots, funnel plots, cumulative meta-analysis plots, moderator plots, diagnostics, and summary tables (CSV / XLSX / TXT)

## Getting Started

### Prerequisites

- **R** (version 4.0.0 or higher)  
- **RStudio** (recommended, but any R environment that can knit R Markdown is fine)  
- The following R packages (the R Markdown file will install missing packages automatically when run):  
  - `metafor` – meta-analysis computations  
  - `tidyverse` – data manipulation and plotting  
  - `ggtext`, `gridExtra`, `broom` – plot styling and model tidying  
  - `knitr`, `xtable` – dynamic report generation and LaTeX tables  
  - `rstudioapi` – locating the project root when run from RStudio  
  - `readxl`, `writexl`, `xfun` – reading/writing Excel and knit utilities  

For strict reproducibility (e.g., journal review), we recommend recording package versions (e.g., via `sessionInfo()` in the paper or using `renv`), even though the script itself installs missing packages automatically.

## Running the Analysis

We recommend using RStudio:

1. Open RStudio.  
2. Open `Code/Meta_Analysis_Markdown.Rmd`.  
3. Knit the document (e.g., click **Knit** → **Knit to HTML** or **Knit to PDF**).  

During knitting, the script will:

- Locate the project root and set paths to `Data/` and `Plots/`.  
- Read `Data/Data_final.xlsx`.  
- Compute effect sizes (Cohen’s *d* / Hedges’ *g*) from multiple types of reported statistics.  
- Fit the main random-effects meta-analysis (REML).  
- Run influence diagnostics, leave-one-out sensitivity, and publication bias checks (Egger’s test, funnel plots, trim-and-fill when \(k \ge 10\)).  
- Generate cumulative meta-analyses by publication year and (if available) study year.  
- Run moderator and meta-regression analyses (LLM model type, interaction type, domain, and combined model).  
- Save all figures and tables to the `Plots/` directory.

## Analysis Components

The meta-analysis includes:

- **Effect size calculations** (standardized mean differences and transformations from *t*, *F*, odds ratios, proportions, and EMMs)  
- **Random-effects meta-analysis** using Hedges’ *g*  
- **Heterogeneity analysis** (e.g., \(\tau^2\), \(I^2\), Q statistics)  
- **Publication bias assessment** (Egger’s test, funnel plots, trim-and-fill when applicable)  
- **Cumulative meta-analysis** by publication year and, if available, by study year  
- **Moderator analyses** for LLM model type, interaction type, and domain, plus a combined meta-regression  
- **Forest plots and additional visualizations** for the main model, cumulative analyses, and moderators  

## Results and Outputs

- The knitted report (HTML/PDF) summarises all analyses.  
- Detailed numerical results, diagnostics, and plots are saved in the `Plots/` directory (e.g., `main_forest_plot_*.pdf`, cumulative plots, moderator coefficient plots, robustness tables).  

These files can be cited or included as supplementary material in the associated manuscript.
