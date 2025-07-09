# MAAR_Stream 
# Reliable Streaming Model Adaptation under Concept Drift Impact Using Multiple Windows


[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/majishah/MAAR_Stream/blob/main/Core_Modified_Adaptability_Household_Drift.ipynb)

## Overview

Historical models perform well on static data. However, maintaining their accuracy over time becomes increasingly difficult, especially in streaming environments characterized by high velocity and continuous change. The primary challenge lies in handling concept drift and ensuring timely adaptation without incurring high computational costs.

To address this, we propose **MAAR** (*Multi-Window and AutoML-based Adaptable Regression*), a resource-efficient framework designed for real-time regression in streaming data. MAAR dynamically detects drift and updates models using asynchronous, AutoML-driven adaptation over multi-window inputs.

Experimental validation confirms that MAAR sustains high predictive accuracy under distributional shifts, making it well-suited for practical deployment in dynamic settings.

## 📁 Dataset

- **Source**: [Individual Household Electric Power Consumption](https://archive.ics.uci.edu/dataset/235/individual+household+electric+power+consumption)
- **Format**: CSV
- **Description**: Records of household energy usage measured every minute over nearly 4 years.
- **Preprocessing**: Subsetting to one-minute resolution and selecting the `Global_active_power` feature.

## 📂 Project Files

├── Core_Modified_Adaptability_Household_Drift.ipynb # Full MAAR implementation in Colab
└── README.md # Project documentation

## ⚙️ Installation (Google Colab)

This notebook is designed to run in **Google Colab**. Before running, install the required libraries:

# Mount Google Drive
from google.colab import drive
drive.mount('/content/drive')

# Install required libraries
!pip install pycaret
!pip install river
⚠️ PyCaret may require a restart of the runtime after installation.

