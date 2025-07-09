# MAAR_Stream 
# Reliable Streaming Model Adaptation under Concept Drift Impact Using Multiple Windows


[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/majishah/MAAR_Stream/blob/main/Core_Modified_Adaptability_Household_Drift.ipynb)

## Overview

Historical models perform well on static data. However, maintaining their accuracy over time becomes increasingly difficult, especially in streaming environments characterized by high velocity and continuous change. The primary challenge lies in handling concept drift and ensuring timely adaptation without incurring high computational costs.

To address this, we propose **MAAR** (*Multi-Window and AutoML-based Adaptable Regression*), a resource-efficient framework designed for real-time regression in streaming data. MAAR dynamically detects drift and updates models using asynchronous, AutoML-driven adaptation over multi-window inputs.

Experimental validation confirms that MAAR sustains high predictive accuracy under distributional shifts, making it well-suited for practical deployment in dynamic settings.

## Dataset

- **Source**: [Individual Household Electric Power Consumption](https://archive.ics.uci.edu/dataset/235/individual+household+electric+power+consumption)
- **Format**: CSV
- **Description**: Records of household energy usage measured every minute over nearly 4 years.
- **Preprocessing**: Subsetting to one-minute resolution and selecting the `Global_active_power` feature.

## 📂 Project Files

├── Core_Modified_Adaptability_Household_Drift.ipynb # Full MAAR implementation in Colab
└── README.md # Project documentation


## Contribution of this work

- ✅ Handles streaming data with concept drift  
- ✅ Multi-window learning for temporal sensitivity  
- ✅ AutoML-based model updating without manual tuning  
- ✅ Suitable for real-time regression in dynamic environments

## Installation (Google Colab)

This notebook is designed to run in **Google Colab**. Before running, install the required libraries:

# Mount Google Drive
from google.colab import drive
drive.mount('/content/drive')

# Install required libraries
!pip install pycaret
!pip install river
⚠️ PyCaret may require a restart of the runtime after installation.

## Results

### Sample Input Data Visualization

<img src="https://raw.githubusercontent.com/majishah/MAAR_Stream/main/images/Input.jpg" width="600"/>


### Drift Detection Example

This plot highlights detected drift points (red) in the streaming power consumption signal.

<img src="https://raw.githubusercontent.com/majishah/MAAR_Stream/main/images/Drift_plot.jpg" width="600"/>

---

### Prediction Accuracy (Actual vs Predicted)

Comparison between the model’s predictions and the real energy usage data.

<img src="https://raw.githubusercontent.com/majishah/MAAR_Stream/main/images/Forecast2.png" width="600"/>


##  Future Work

 - Extend to classification-based streaming tasks  
 - Adapt to evolving feature spaces
 - Incorporate Interpretability to it
 - Embed in stream processing systems (Kafka, Flink) 


