This repository contains the complete R-code for a Cost-effectiveness analysis comparing FemBloc® (novel permanent contraceptive device) to Tubal Ligation (TL) for permanent contraception for Norwegian women aged 25-50. The analyysis is conducted from an extended healthcare perspective incorporating direct medical costs, travel expenses and lost leisure time in accordance with NoMA guidelines. This analysis was conducted as part of an academic thesis, Femasys Inc. had no role in the design, analysis, results nor discussion. 

# Key Features 

- Hybrid model: Decision tress + Markov Model
- 25 Year Time Horizon
- Age stratification by 5 year bands
- Fecundity Decay emperically derived exponential decline at 2.765% annaully
- Comprehensive uncertainty: DSA, PSA, EVPPI
- Outcomes: QALYs, Unintended pregnancies
- Sub-Group analysis

# Repository structure

- FemBloc_CEA_2.Rmd              # Main R Markdown script
- Appendix_Table_Fecundity_PSA.docx   # Fecundity parameters
- Table2_UP_Conditional_Probabilities.docx  # UP outcome probabilities
- Appendix_UP_PSA_Parameters.csv         # PSA parameters
- fembloc_results_tables.docx            # All results tables
- fembloc_ce_plane.png                   # CE plane (QALY)
- fembloc_ce_plane_UP.png                # CE plane (UP)
- fembloc_ceac.png                       # CEAC (QALY)
- fembloc_ceaf.png                       # CEAF (QALY)
- fembloc_ceaf_UP.png                    # CEAF (UP)
- fembloc_evppi.png                      # EVPPI curve
- fembloc_tornado.png                    # Tornado plot
- fembloc_psa.RData                      # PSA results cache
- fembloc_evppi.RData                    # EVPPI results cache
- fembloc_scenarios.RData                # Scenario results cache

# R packages required

library(dplyr)
library(ggplot2)
library(knitr)
library(kableExtra)
library(flextable)
library(officer)
library(mice)          # Multiple imputation
library(MCMCpack)      # Dirichlet distribution
library(dampack)       # CEAC, CEAF, tornado plots
library(mgcv)          # GAM for EVPPI
library(coda)          # Convergence diagnostics
library(zoo)           # Rolling statistics

# Citation

Omondi, N.A (2026). Cost-Effectiveness of FemBloc® VS Tubal Ligation for permanent contraception in Norwegian women aged 25-50: A 25-year Hybrid Decision-Tree Markov Model. [Thesis/Dissertation]. University Of Oslo. Erasmus University Rotterdam. 
ORCID: 0009-0000-0168-545X.

