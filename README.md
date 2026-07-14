# Non-Linear Modeling of Genotype × Environment Interaction

This repository provides the reproducible analytical workflow associated with the study **“Non-Linear Modeling of Genotype × Environment Interaction via Tree-Based Learning Algorithms and Shapley Decomposition.”**

## Authors

**Moyses Nascimento**  
Associate Professor  
Department of Statistics — Federal University of Viçosa  
[moysesnascim@ufv.br](mailto:moysesnascim@ufv.br)

**Weverton Gomes da Costa**  
Postdoctoral Researcher  
Department of Statistics — Federal University of Viçosa  
[weverton.costa@ufv.br](mailto:weverton.costa@ufv.br)

## Overview

Genotype-by-environment interaction is a central component of multi-environment trial analysis because genotypes may respond differently across environmental conditions.

This project combines tree-based machine learning, Shapley Additive Explanations, and AMMI-based methods to evaluate genotype performance, adaptability, responsiveness, and stability.

The complete analytical workflow is presented in a single R Markdown document and published as a version-controlled `workflowr` research website.

## Analytical workflow

The analysis includes:

1. import and preparation of multi-environment trial data;
2. visualization of phenotypic performance;
3. calculation of the environmental index;
4. Random Forest fitting and leave-one-environment-out validation;
5. SHAP decomposition of model predictions;
6. AMMI decomposition of genotype-by-environment interaction;
7. calculation of the AMMI Stability Value;
8. calculation of SHAP effect and stability measures;
9. simultaneous selection and genotype ranking;
10. visualization of genotype-rank dynamics;
11. concordance between linear and non-linear stability rankings;
12. Spearman rank correlation among selection criteria.

## Data

The analysis uses a maize multi-environment trial data set containing:

- 9 genotypes;
- 20 environments;
- 4 replicates per genotype-by-environment combination;
- 720 original observations;
- grain yield measured in kilograms per hectare.

The original data file is stored in:

```text
data/maize.txt
```

The variables are:

| Variable | Description |
|---|---|
| `ENV` | Environment identifier |
| `GEN` | Genotype identifier |
| `REP` | Replicate identifier |
| `GY` | Grain yield in kilograms per hectare |

## Repository structure

```text
nonlinear-ge-interaction-shap/
├── analysis/
│   ├── _site.yml
│   ├── index.Rmd
│   ├── analysis.Rmd
│   ├── about.Rmd
│   └── license.Rmd
├── code/
├── data/
│   └── maize.txt
├── docs/
├── output/
│   ├── random_forest_loeo_predictions.rds
│   └── shap_results.rds
├── README.md
├── _workflowr.yml
└── nonlinear-ge-interaction-shap.Rproj
```

## Reproducible analysis

The complete analytical pipeline is available in:

```text
analysis/analysis.Rmd
```

All analytical code is displayed directly in the analysis page.

The computationally intensive Random Forest validation and SHAP calculations are preserved as visible code with `eval = FALSE`. Their previously calculated and validated results are stored as version-controlled R objects:

```text
output/random_forest_loeo_predictions.rds
output/shap_results.rds
```

Hidden loading chunks read these objects during routine website construction. This structure preserves the complete analytical procedure while avoiding repeated execution of computationally intensive steps.

The loaded objects are checked for:

- file availability;
- expected dimensions;
- expected variable names;
- genotype and environment factor levels;
- absence of missing values.

## Website

Project website:

```text
https://wevertongomescosta.github.io/nonlinear-ge-interaction-shap/
```

Complete analysis:

```text
https://wevertongomescosta.github.io/nonlinear-ge-interaction-shap/analysis.html
```

## Reproducibility framework

The project is managed with the `workflowr` R package. The framework integrates:

- R Markdown documents;
- Git version control;
- reproducibility checks;
- recorded session information;
- relative file paths;
- versioned figures and results;
- a static research website.

Each published page is connected to the Git commit containing the corresponding analytical source code.

## Software requirements

The analysis requires:

- R;
- RStudio or another R Markdown-compatible environment;
- Git;
- `workflowr`;
- `ggplot2`;
- `dplyr`;
- `tidyr`;
- `randomForest`;
- `DALEX`;
- `patchwork`;
- `ggrepel`;
- `corrplot`;
- `viridisLite`.

## Reproducing the project

Clone the repository:

```bash
git clone https://github.com/WevertonGomesCosta/nonlinear-ge-interaction-shap.git
```

Open the R project:

```text
nonlinear-ge-interaction-shap.Rproj
```

Build the complete website:

```r
workflowr::wflow_build()
```

Build only the analytical page:

```r
workflowr::wflow_build(
  "analysis/analysis.Rmd"
)
```

View the local website:

```r
workflowr::wflow_view()
```

## Project context

This work is developed in connection with the [LICAE Laboratory](https://www.licae.ufv.br/) and the Department of Statistics at the Federal University of Viçosa.

## License

Except where otherwise indicated, the materials in this repository are distributed under the **Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License — CC BY-NC-SA 4.0**.

The complete licensing conditions are available on the project website:

```text
https://wevertongomescosta.github.io/nonlinear-ge-interaction-shap/license.html
```

## Suggested citation

Nascimento, M. and Costa, W. G. (2026). *Non-Linear Modeling of Genotype × Environment Interaction via Tree-Based Learning Algorithms and Shapley Decomposition*. Workflowr project website and analytical repository. Available at: https://wevertongomescosta.github.io/nonlinear-ge-interaction-shap/

When scientific methods, results, or interpretations from the associated manuscript are reused, the final published manuscript should also be cited.

## Contact

**Moyses Nascimento**  
Department of Statistics — Federal University of Viçosa  
[moysesnascim@ufv.br](mailto:moysesnascim@ufv.br)

**Weverton Gomes da Costa**  
Department of Statistics — Federal University of Viçosa  
[weverton.costa@ufv.br](mailto:weverton.costa@ufv.br)