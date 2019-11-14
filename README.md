# File Hierarchy
  ``` bash
  ├── Makefile
  ├── README.md
  ├── data
  │   ├── cleaned
  │   ├── processed
  │   └── raw
  │       ├── booking_log.csv
  │       ├── experiment_log.csv
  │       ├── participant_log.csv
  │       └── test_data.csv
  ├── model 
  │   └── xgboost_model_v1
  ├── notebooks
  │   ├── 0.0-jean-basic-metrics-computation.ipynb
  │   ├── 0.0-jean-basic-metrics-computation.py
  │   ├── 1.0-jean-initial-data-cleaning-and-exploration.ipynb
  │   ├── 1.0-jean-initial-data-cleaning-and-exploration.py
  │   ├── 2.0-jean-feature-engineering-selection.ipynb
  │   ├── 2.0-jean-feature-engineering-selection.py
  │   ├── 3.0-jean-modeling.ipynb
  │   ├── 3.0-jean-modeling.py
  │   ├── 4.0-jean-simulation-conclusion.ipynb
  │   └── 4.0-jean-simulation-conclusion.py
  └── requirements.txt
  ```
# Set up
Data are removed from the submission, in order to run Makefile, replace **booking_log.csv, experiment_log.csv, participant_log.csv, test_data.csv** under **./data/raw/**
  
# Reproduce results
run command **make** under the current directory
  
# Key files
There are 5 notebooks under folder notebooks:
1. 0.0-jean-basic-metrics-computation.ipynb - For basic metrics calculation
2. 1.0-jean-initial-data-cleaning-and-exploration.ipynb - Data cleaning and initial exploration
3. 2.0-jean-feature-engineering-selection.ipynb - Feature engineering mainly for two parts: trip related and driver related
4. 3.0-jean-modeling.ipynb - Hyperparameter tuning and model selection
5. 4.0-jean-simulation-conclusion.ipynb - Simulation on test data, model limitationa and further improvement

# Side notes
Our objective is to reduce the cancellation after we find the driver. Thus, the evaluation metric should be precision (TP/(TP+NP)) which is (# complete/ (# predicted as complete so assign the driver)).
For further details, please refer to the notebook comments.
