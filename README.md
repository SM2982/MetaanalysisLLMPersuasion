# Meta-Analysis of LLMs and Persuasion

This repository contains the code, data, and analysis for a meta-analysis investigating the persuasive effectiveness of Large Language Models (LLMs) compared to human communicators.

## Repository Structure

- `Code/` - Contains all analysis scripts and code
- `Data/` - Raw and processed data used in the meta-analysis
- `Plots/` - Generated visualizations and plots
- `Submission/` - Final compiled PDF document and submission materials

## Getting Started

### Prerequisites

- R (version 4.0.0 or higher)  
- RStudio (recommended IDE for running the analysis)  
- Required R packages (will be automatically installed when running the code):  
  - `metafor` – For meta-analysis computations  
  - `tidyverse` – For data manipulation and visualization  
  - `ggtext` – For enhanced text formatting in plots  
  - `gridExtra` – For arranging multiple plots  
  - `broom` – For tidying statistical models  
  - `knitr` – For dynamic report generation  
  - `xtable` – For creating LaTeX tables  
  - `rstudioapi` – For RStudio integration
  - `readxl` – For importing Excel files  
  - `writexl` – For exporting data to Excel  

## Running the Analysis

We recommend using RStudio to run the analysis:

1. Open RStudio  
2. Open the main analysis file (`Code/Meta_Analysis.R`)  
3. Run the code:  
   - **macOS**: Select all code (`⌘ + A`) and run  
   - **Windows**: Select all code (`Ctrl + A`) and run  

## Analysis Components

The meta-analysis includes:

- Effect size calculations  
- Heterogeneity analysis  
- Publication bias assessment  
- Moderator analyses  
- Forest plots and other visualizations  

## Results

Key findings and visualizations can be found in the `Plots/` directory. 
