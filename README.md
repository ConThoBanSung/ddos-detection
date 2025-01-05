# DDoS Detection System

## Overview
This project implements a system for detecting and classifying **DDoS (Distributed Denial of Service)** attacks using the **CICDDoS2019** dataset. The objective is to build a multiclass classification model that distinguishes between various types of DDoS attacks and normal network traffic.

## Dataset
The **CICDDoS2019** dataset, provided by the Canadian Institute for Cybersecurity (CIC), contains labeled network traffic data, including:
- **Syn**: SYN flood attack.
- **Benign**: Normal, non-attack traffic.
- **Portmap**, **UDP**, **UDPLag**, **MSSQL**, **NetBIOS**, **LDAP**: Various DDoS attack types.

### Key Features:
- **Packet Sizes**
- **Source/Destination IPs**
- **Protocol Types**

## Project Workflow
1. **Data Collection and Preprocessing**:
   - Align column names between training and testing datasets.
   - Handle null values and remove duplicates.
   - Remove low-information and highly correlated features.

2. **Exploratory Data Analysis (EDA)**:
   - Visualize traffic distribution across attack labels and protocols.
   - Analyze key attributes like flow duration and packet lengths.
   - Correlation heatmap for feature selection.

3. **Feature Engineering**:
   - Split data into training, validation, and testing sets.
   - Encode target labels using `LabelEncoder`.
   - Scale features using Min-Max Scaling.

4. **Model Training and Evaluation**:
   - Algorithms tested:
     - Random Forest
     - K-Nearest Neighbors (KNN)
     - Extra Trees Classifier
     - Multi-Layer Perceptron (MLP)
     - XGBoost
   - Evaluation metrics:
     - Accuracy
     - Precision
     - Recall
     - F1-Score
     - ROC AUC
   - ROC curves for multiclass classification.

5. **Results Visualization**:
   - Compare model performance via accuracy scores and ROC curves.

## Getting Started

### Prerequisites
- Python 3.7+
- Required libraries:
  - `pandas`
  - `numpy`
  - `matplotlib`
  - `seaborn`
  - `sklearn`
  - `xgboost`

### Installation
1. Clone this repository:
   ```bash
   git clone <repository_url>
   cd ddos-detection
   ```
2. Install required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

### Running the Project
1. Open the notebook file:
   ```bash
   jupyter notebook ddos_detection.ipynb
   ```
2. Execute the cells step-by-step to preprocess data, train models, and visualize results.

## Results
- Performance metrics for each algorithm are presented.
- ROC curves highlight model classification ability across attack types.

## Future Work
- Extend the dataset with real-time traffic.
- Implement additional algorithms like CNNs or LSTMs for improved detection.
- Optimize feature selection using advanced methods.

## License
This project is licensed under the MIT License. See the `LICENSE` file for details.
