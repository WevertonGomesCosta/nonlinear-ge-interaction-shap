# Non-Linear Modeling of Genotype × Environment Interaction

This repository provides a reproducible `workflowr` tutorial associated with the study **“Non-Linear Modeling of Genotype × Environment Interaction via Tree-Based Learning Algorithms and Shapley Decomposition.”**

## Overview

Genotype-by-environment interaction is a central component of multi-environment trial analysis because genotypes may respond differently across environmental conditions.

This project presents an analytical workflow that combines tree-based machine learning, Shapley Additive Explanations, and traditional AMMI-based methods to evaluate genotype performance, adaptability, and stability.

The repository is organized as a reproducible tutorial in which the complete analytical pipeline is presented in an R Markdown document.

## Objectives

The analytical workflow is structured to:

1. summarize phenotypic performance across genotypes and environments;
2. fit and validate a tree-based machine learning model;
3. obtain local feature contributions through SHAP decomposition;
4. perform AMMI decomposition of genotype-by-environment interaction;
5. calculate stability and simultaneous selection indices;
6. compare genotype rankings across linear and non-linear frameworks;
7. evaluate rank concordance using Spearman correlation.

## Data

The analysis uses a maize multi-environment trial data set containing:

- 9 genotypes;
- 20 environments;
- 4 replicates per genotype-by-environment combination;
- grain yield measured in kilograms per hectare.

The original data file is stored in:

```text
data/maize.txt
```

## Repository structure

```text
nonlinear-ge-interaction-shap/
├── analysis/
│   ├── _site.yml
│   ├── index.Rmd
│   ├── about.Rmd
│   └── license.Rmd
├── code/
├── data/
├── docs/
├── output/
├── LICENSE
├── README.md
├── _workflowr.yml
└── nonlinear-ge-interaction-shap.Rproj
```

The complete analytical page will be added as:

```text
analysis/analysis.Rmd
```

## Reproducibility

The project is managed with the `workflowr` R package. The framework combines:

- R Markdown documents;
- Git version control;
- reproducibility checks;
- versioned results;
- a static research website.

All analytical code will be displayed directly in the analysis page. No external analytical functions or hidden execution scripts are required to reproduce the workflow.

## Website

The project website is available at:

```text
https://wevertongomescosta.github.io/nonlinear-ge-interaction-shap/
```

## Software requirements

The analysis requires:

- R;
- RStudio or another R Markdown-compatible environment;
- Git;
- workflowr;
- the R packages listed in the analysis page.

## Reproducing the project

Clone the repository:

```bash
git clone https://github.com/WevertonGomesCosta/nonlinear-ge-interaction-shap.git
```

Open:

```text
nonlinear-ge-interaction-shap.Rproj
```

Build the website from the R console:

```r
workflowr::wflow_build()
```

View the local website:

```r
workflowr::wflow_view()
```

## Associated manuscript

The original manuscript associated with the analytical workflow will be preserved in the repository without modification.

## License

Except where otherwise indicated, the materials in this repository are licensed under the Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License.