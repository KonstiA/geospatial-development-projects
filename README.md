# Geospatial Analysis of development projects in R
Geospatial analysis of the effects of development projects on institutional legitimacy in Africa (Afrobarometer &amp; World Bank Project Data)

This repository contains R scripts used for the data analysis. It includes:

- Data preprocessing
- Statistical analysis (e.g., regressions, hypothesis testing)
- Data visualization
- Robustness checks

## How to Use
1. Clone the repository.
2. Install the required R packages: `foreign`, `readr`, `readxl`, `tidyverse`, `broom`, `stringr`, `dplyr`, `skimr`, `officer`, `flextable`, `sf`, `sjlabelled`, `ggplot2`, `fixest`, `texreg`, `rnaturalearth`, `rnaturalearthdata`, `countrycode`.
4. Run `geospatial-development-projects.Rmd` for the main results.

## Highlights
- Modular, reusable code.
- Example of geospatial regression modeling and data visualization in R.

# Thematic project Description
Foreign Aid and Institutional Quality in Africa: Evidence from Afrobarometer and World Bank Project Data || A Geospatial Analysis of the Effects of World Bank Development Projects on Perceived Institutional Legitimacy.

Abstract
- This study analyses the impact of World Bank development projects on citizens' perceptions of institutional legitimacy and their sense of obligation to comply with key state institutions in Africa. Using location data from 28 African countries between 2008 and 2014 and a difference-in-difference-like analysis of a sample of approximately 61,000 citizens, it examines how these projects affect institutional legitimacy. Grounded in Legitimacy Theory, the results demonstrate that development projects generally enhance institutional legitimacy by improving procedural fairness and increasing institutional performance. However, the effects vary depending on the project themes, proximity to citizens and project status. For example, completed projects tend to strengthen the legitimacy of the police, while ongoing projects have a negative effect on the legitimacy of the courts. The study emphasises the complexity of the relationship between development projects and institutional legitimacy and highlights the need for nuanced approaches in policy and implementation.

Analysis
- The primary dependent variable is a binary indicator of citizens’ willingness to comply with three key formal institutions, based on their agreement or disagreement with the following statements: “The courts have the right to make decisions that people always have to abide by,” “The police always have the right to make people obey the law,” and “The tax authorities always have the right to make people pay taxes.” As outlined by Levi et al., these Afrobarometer questions are appropriate to capture the concept of legitimacy, reflecting a sense of obligation or willingness to comply with institutional authority (Levi et al., 2009).

- The main independent variables are three dummy variables created by merging datasets to determine whether a respondent lived within a specified distance of an ongoing, completed, or future World Bank project, thereby being considered “treated.” Specifically, this involved measuring the distance from a cluster centre point, where around eight respondents were surveyed, to project locations. If at least one project was located within the cut-off distance, a dummy variable was assigned for each benchmark. For robustness checks, these three dummy variables were created for cut-off distances of 10 km, 20 km, and 30 km, respectively.

Identification Strategy
- We use a difference-in-difference-like measure as our effect identification strategy, specifically a spatial-temporal estimation. This approach builds on the foundational work of Kotsadam and Tolonen, as well as Knutsen et al., in their studies on mining, local employment, and corruption in Africa, and has been further adjusted by Isaksson and Durevall for project data analysis (Isaksson & Durevall, 2023; Knutsen et al., 2017; Kotsadam & Tolonen, 2016).
