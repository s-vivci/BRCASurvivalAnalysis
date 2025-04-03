# BRCA Survival Analysis

## Project Overview

This project conducts a survival analysis on Breast Cancer (BRCA) data sourced from the METABRIC Group, obtained via [cBioPortal](https://www.cbioportal.org/). The analysis encompasses:

- **Exploratory Data Analysis (EDA):** Data cleaning and initial examination.
- **Kaplan-Meier Estimation:** Non-parametric survival function estimation stratified by age and tumor stage.
- **Log-Rank Test:** Comparison of survival distributions based on chemotherapy status.
- **Cox Proportional Hazards Model:** Regression modeling to assess the impact of variables like HER2 status and tumor size on survival times.
- **Machine Learning Approaches:** Implementation of Random Survival Forests to predict survival probabilities and evaluate variable importance.

## Data Source

The dataset used in this analysis is the BRCA METABRIC clinical data, downloaded from [cBioPortal](https://www.cbioportal.org/). It includes comprehensive clinical information pertinent to breast cancer patients.

## Repository Structure

- `brca_survival_analysis.Rmd`: Main R Markdown notebook containing the analysis.
- `brca_metabric_clinical_data.tsv`: Raw dataset used for the analysis.
- `VIMPsur.png`: Visualization of Variable Importance from the Random Survival Forest model.

## Installation and Setup

To replicate this analysis:

1. **Install Required Libraries:**

   ```r
   install.packages(c("randomForestSRC", "ggsurvfit", "survival", "survminer", "data.table", "mltools", "skimr", "knitr", "dplyr", "tidyverse", "readr", "ggplot2", "tibble"))
   ```

2. **Clone the Repository:**

   ```bash
   git clone https://github.com/yourusername/brca_survival_analysis.git
   ```

3. **Set Working Directory:**

   ```r
   setwd("path/to/brca_survival_analysis")
   ```

4. **Run the Analysis:**

   Open `brca_survival_analysis.Rmd` in RStudio and knit the document to produce the analysis output.

## Usage

The R Markdown notebook is structured into distinct sections, each focusing on a specific aspect of the survival analysis. Users can navigate through the sections to understand the methodology and replicate the results.

## Results

Key findings from the analysis include:

- **Kaplan-Meier Curves:** Visualizations indicating survival probabilities stratified by age groups and tumor stages.
- **Log-Rank Test:** Statistical comparison showing significant survival differences based on chemotherapy status.
- **Cox Proportional Hazards Model:** Identification of HER2 positive status and larger tumor size as significant factors associated with increased hazard rates.
- **Random Survival Forest:** Prediction models highlighting the importance of variables like relapse-free status, age, and number of positive lymph nodes in determining survival outcomes.

## Contributing

Contributions to enhance this analysis are welcome. Please fork the repository and submit a pull request with your proposed changes.

## License

This project is licensed under the [MIT License](LICENSE).

## References

- Curtis C, Shah SP, Chin SF, et al. The genomic and transcriptomic architecture of 2,000 breast tumours reveals novel subgroups. *Nature*. 2012;486(7403):346-352. doi:10.1038/nature10983.
- Cerami E, Gao J, Dogrusoz U, et al. The cBio Cancer Genomics Portal: An Open Platform for Exploring Multidimensional Cancer Genomics Data. *Cancer Discovery*. 2012;2(5):401-404. doi:10.1158/2159-8290.CD-12-0095.
- Gao J, Aksoy BA, Dogrusoz U, et al. Integrative analysis of complex cancer genomics and clinical profiles using the cBioPortal. *Science Signaling*. 2013;6(269):pl1. doi:10.1126/scisignal.2004088.
- de Bruijn S, Ritchie ME, Carvalho BS, et al. Analysis and Visualization of Longitudinal Genomic and Clinical Data from the AACR Project GENIE Biopharma Collaborative in cBioPortal. *Cancer Research*. 2023. doi:10.1158/0008-5472.CAN-22-3456.
- Abadi A, Yavari P, Dehghani-Arani M, et al. Cox models survival analysis based on breast cancer treatments. *Iran J Cancer Prev*. 2014;7(3):124-129.

