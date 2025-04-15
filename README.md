# System-Threat-Forecaster Kaggle Competition:

## Overview

The goal of this competition was to predict the probability that a system is infected by various families of malware based on its telemetry data. This data was generated from threat reports collected by antivirus software installed on the machines. Each machine is identified by a unique `MachineID`, and the target variable indicates whether malware was detected.

I developed a solution that achieved a **Rank of 51** out of 1500+ participants, showcasing robust data preprocessing, feature engineering, and ensemble modeling techniques.

## Competition Details

- **Objective:** Predict whether a machine is infected with malware.
- **Dataset Files:**
  - `train.csv` – Training dataset with system telemetry data and ground truth labels.
  - `test.csv` – Test dataset for which predictions need to be generated.
  - `sample_submission.csv` – A sample submission file in the correct format.

## Data Description 📚

The dataset includes a wide variety of features extracted from system telemetry, including:

- **MachineID:** Unique Identifier for each machine.
- **ProductName:** Name of the installed antivirus product.
- **EngineVersion, AppVersion, SignatureVersion:** Version information for the antivirus software.
- **IsBetaUser:** Indicator if the user is on a beta version.
- **RealTimeProtectionState, IsPassiveModeEnabled:** System protection states.
- **AntivirusConfigID:** Identifier for the antivirus configuration.
- **System Specifications:** Details such as OS version, build number, processor information, and more.
- **Geographical and Locale Information:** Columns like `CountryID`, `CityID`, and `GeoRegionID`.
- **Timestamp Features:** `DateAS` (malware signature dates) and `DateOS` (OS update timestamps).
- **target:** The ground truth indicating if malware was detected.

For a full list of features, please refer to the dataset documentation.

## Approach 💻

### 1. Data Preprocessing

- **Missing Value Handling:** Identified and appropriately imputed or removed missing values.
- **Data Cleaning:** Removed redundant and noisy features to enhance model performance.
- **Feature Engineering:** Extracted new features from timestamps, version strings, and categorical variables to better capture the behavior of each system.

### 2. Exploratory Data Analysis (EDA)

- Conducted thorough EDA to understand the data distribution and correlations.
- Visualized feature relationships to identify patterns and potential predictors of malware infection.

### 3. Modeling

- **Model Selection:** Tested several models, including popular tree-based models like XGBoost and LightGBM.
- **Ensemble Methods:** Combined multiple models to improve prediction robustness and generalization.
- **Validation:** Used cross-validation techniques to validate model performance and mitigate overfitting.

### 4. Final Submission

- Generated final predictions for the test dataset.
- Tuned model parameters and thresholds to optimize the chosen performance metric.
- Submitted the predictions to Kaggle and secured a top ranking among 1500+ competitors.

## Achievements ✅

- **Rank:** Achieved **51st place** in the competition.
- **Impact:** Demonstrated strong skills in data science, machine learning, and practical problem solving in the field of cybersecurity.
- **Innovation:** Developed an end-to-end solution that balances performance with interpretability.

## How to Run the Project

To reproduce or extend this project, follow these steps:

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/Mayank8IITM/System-Threat-Forecaster----ML-Project.git
2. **Run the Notebook:**
3.  ```bash
    jupyter notebook 23f1000598-notebook-t12025.ipynb
  
 
