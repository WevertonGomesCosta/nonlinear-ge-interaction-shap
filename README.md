# Non-Linear Modeling of Genotype × Environment Interaction

This repository provides the reproducible analytical workflow associated with the study **“Non-Linear Modeling of Genotype × Environment Interaction via Tree-Based Learning Algorithms and Shapley Decomposition.”**

## Authors

**Moysés Nascimento¹\***  
**Weverton Gomes da Costa¹**  
**Ana Carolina Campana Nascimento¹**  
**Noé Mitterhofer Eiterer Ponce de Leon da Costa²**  
**Diego Jarquín³**

\*Corresponding author: [moysesnascim@ufv.br](mailto:moysesnascim@ufv.br)

### Affiliations

¹ Laboratory of Computational Intelligence and Statistical Learning (LICAE), Department of Statistics, Federal University of Viçosa (UFV), Viçosa, Minas Gerais, Brazil.

² Agronomy Department, Federal University of Tocantins (UFT), Gurupi, Tocantins, Brazil.

³ Agronomy Department, University of Florida, Gainesville, Florida, USA.

## Overview

Genotype-by-environment interaction is a central component of multi-environment trial analysis because genotypes may respond differently across environmental conditions.

This project combines tree-based machine learning, Shapley Additive Explanations, and AMMI-based methods to evaluate genotype performance, adaptability, responsiveness, and stability.

The complete analytical workflow is presented in a single R Markdown document and published as a version-controlled `workflowr` research website.

## Analytical workflow

The analysis includes:

1. import and preparation of multi-environment trial data;
2. graphical representation of the leave-one-environment-out validation scheme;
3. visualization of phenotypic performance;
4. calculation of the environmental index;
5. Random Forest fitting and leave-one-environment-out validation;
6. SHAP decomposition of model predictions;
7. AMMI decomposition of genotype-by-environment interaction;
8. calculation of AMMI and SHAP stability measures;
9. calculation of classical and SHAP-based simultaneous selection indices;
10. genotype ranking across six selection criteria;
11. visualization of genotype-rank dynamics;
12. Spearman rank correlation among the six selection criteria.

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

All analytical code, outputs, tables, and figures are presented on the analysis page.

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
- `iBreakDown`;
- `pals`;
- `ggh4x`;
- `ggcorrplot`.

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

Nascimento, M., Costa, W. G., Nascimento, A. C. C., Costa, N. M. E. P. L., and Jarquín, D. (2026). *Non-Linear Modeling of Genotype × Environment Interaction via Tree-Based Learning Algorithms and Shapley Decomposition*. Workflowr project website and analytical repository. Available at: https://wevertongomescosta.github.io/nonlinear-ge-interaction-shap/

When scientific methods, results, or interpretations from the associated manuscript are reused, the final published manuscript should also be cited.

## Contact

**Corresponding author**

**Moysés Nascimento**  
Laboratory of Computational Intelligence and Statistical Learning (LICAE)  
Department of Statistics — Federal University of Viçosa  
[moysesnascim@ufv.br](mailto:moysesnascim@ufv.br)

**Repository contact**

**Weverton Gomes da Costa**  
Laboratory of Computational Intelligence and Statistical Learning (LICAE)  
Department of Statistics — Federal University of Viçosa  
[weverton.costa@ufv.br](mailto:weverton.costa@ufv.br)