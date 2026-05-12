Project Overview

This project replicates and extends the study “The Gender Gap in Self-Promotion” (Exley & Kessler, 2022), which finds that women tend to rate their performance lower than equally capable men. Our work:
Replicates the original experiment using main.dta.
Extends the analysis to Canada’s PIAAC survey data to examine self-promotion patterns among working adults.
Explores how education and age influence the self-promotion gap.
Validates findings by comparing results across the original and PIAAC datasets.

Folder Structure
team_9_code.zip/
└── Project/
    ├── .Rproj.user/
    ├── data/
    │   ├── employers_long.dta
    │   ├── main.dta
    │   ├── payoffs_long.dta
    │   ├── predictors.dta
    │   └── prgcanada.csv
    ├── .Readme.txt
    ├── .RData
    ├── .RDataTmp
    ├── .Rhistory
    └── team_9_code.rmd

/data        - Raw data files (main.dta, prgcanada.csv)
/figures     - Output plots (CDFs, gap plots, sensitivity analyses)
/models      - Saved RDS model objects
/README.md   - Project overview and instructions

Requirements:
≥ R 4.0 Version
Packages: tidyverse, haven, janitor, survey, modelsummary,marginaleffects, kableExtra, tibble, broom, purrr, glue, patchwork, sandwich, lmtest,
          fitdistrplus, caret, gt, webshot2, flextable, officer, gridExtra, grid.
Code Chunk	                Seed	One-line Description
0_global_setup	                123	Load packages, set options, and initialize global seed for reproducibility.
1.1_Figure 1-cdf_plots	        123	Generate ECDF plots for performance, belief, and self-promotion gap by gender.
1.2.1_Table_2-Panel_A           123	runs OLS and exports HTML/TEΧ tables, Computes & prints a summary table of estimates/SEs/p-values.
1.2.2_format_table	        123	Format regression results into journal-style tables for reporting.
1.3.1-1.3.3_Diagnostic Checks           Verify data quality, handle unequal sample sizes, and confirm robustness.specifications.
2.1_build_piacc_dataset	        6092	Clean PIAAC Canada dataset and construct survey design with BRR weights.
2.2_weighted_regression_table	6092	Run weighted regressions for gender gap by education and age.
2.3_weighted_cdf_plots	        6092	Plot weighted CDFs for numeracy performance, usage, and self-promotion gaps.
2.4_gap_by_edu_age	        6092	Plot predicted gender gap by education levels and age groups.
3.1_validate_replication_models	123	Run replication regressions to validate PIAAC results using original experiment data.
3.2_coeff_comparison_table      123	Present female, age, and education coefficients across multiple model specifications.
3.3_gap_vs_education_continuous	123	Visualize interaction of gender and continuous education on self-promotion gap.
A1_sensitivity_edu_split	123	Examine how gender gap changes across different education cutpoints in sensitivity analysis.
A2.1-A2.2_Heterogeneity Analysis 

Reproducing Results:
Place all datasets in the /data folder.
Run the R script code chunks in the /team_9_code.rmd in the following order:
replication_analysis
run the diagnostics_checks 
extension1_piaac_dataset
extension2_edu_age_analysis
Heterogeneity Analysis _ Original paper (optional)

Figures and tables will be automatically saved in the /figures folder.
Key outputs include:
figure1_*.png – Replication CDF plots
table2_panelA_result.html / .tex – Replication regression tables
fig_cdf_*.png – Weighted PIAAC plots
fig_gap_by_*.png – Self-promotion gap by education/age
models_piacc_gender_gap_brr.rds – Saved PIAAC regression models


Notes:
All analyses are reproducible using the specified seeds.
Weighted analyses use BRR survey weights for PIAAC data.



