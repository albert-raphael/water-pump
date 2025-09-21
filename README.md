# Water Pump Functionality Prediction (On Going Project)
**By Assimagbe Albert Raphael**

<img src="Image/hand_pump_diagram.png"/>

## Overview

This project uses machine learning to predict the operational status of water pumps in rural communities. Based on demographic, geographic, and technical features, the model classifies pumps into three categories:

* **Functional**
* **Needs repair**
* **Non-functional**

The aim is to support maintenance teams, local planners, and NGOs by providing actionable insights and geospatial visualizations, enabling better allocation of resources and faster response times.

## Project Goals

1. Develop classification models to predict pump functionality.
2. Analyze key factors that influence pump performance.
3. Create geospatial visualizations to highlight regional patterns of failures.
4. Deploy a simple dashboard to showcase predictions and insights.

## Dataset

The dataset includes information on pump location, construction, installer, and management details, along with labels for functionality status. Files provided:

* `Training_set_values.csv` — feature data for training.
* `Training_set_labels.csv` — target labels for pump functionality.
* `Test_set_values.csv` — feature data for testing and model evaluation.

## Data Description

### Dataset Source
The data comes from Taarifa and the Tanzanian Ministry of Water, which aggregates information about water points across Tanzania.

### Features Overview
The dataset contains 40+ columns representing:
- Geographic information (coordinates, region, basin)
- Technical specifications (pump type, extraction method)
- Management details (installer, funder, payment type)
- Water characteristics (quality, quantity, source)
- Temporal information (construction year, recording date)

## Workflow

1. **Data Exploration** — assess distributions, missing values, and feature-target relationships.
2. **Feature Engineering** — create meaningful features (e.g., pump age, regional aggregates).
3. **Model Development** — train and validate classifiers such as Random Forest, XGBoost, or LightGBM.
4. **Insights** — interpret feature importance, highlight regional disparities, and provide actionable findings.
5. **Deployment** — publish an interactive dashboard (Streamlit/Dash) with predictions, maps, and key metrics.

## Deliverables

* Cleaned datasets and preprocessing pipeline.
* Trained model artifacts.
* Performance reports and visualizations.
* Dashboard application for stakeholders.

## Installation & Usage

```bash
# Clone repository
git clone https://github.com/albert-raphael/water-pump.git
cd water-pump

# Install dependencies
pip install -r requirements.txt

# Run training script
python train_model.py

# Launch dashboard
streamlit run app.py
```
## Competition Link
[DrivenData - Pump it Up: Data Mining the Water Table](https://www.drivendata.org/competitions/7/pump-it-up-data-mining-the-water-table/)

## Project Structure

### 1: Exploratory Data Analysis
- Clean and preprocess the dataset
- Handle missing values and categorical variables
- Create geospatial visualizations of water pump distribution
- Analyze relationships between features and pump functionality
- **Deliverable**: EDA report with visualizations and initial insights

### 2: Model Development
- Feature engineering and selection
- Train baseline classification models
- Implement cross-validation and hyperparameter tuning
- Evaluate models using appropriate classification metrics
- **Deliverable**: Trained models with documented performance metrics

### 3: Insights & Deployment
- Analyze feature importance and model explanations
- Create a Streamlit dashboard with interactive maps
- Document findings and recommendations for maintenance strategies
- **Deliverable**: Interactive dashboard and final presentation

### Required Libraries
```
pandas
numpy
scikit-learn
matplotlib
seaborn
geopandas
folium
streamlit
plotly
```

## Technical Requirements

### Required Technologies
- Python (pandas, scikit-learn, matplotlib/seaborn)
- Geospatial libraries (GeoPandas, Folium)
- Jupyter Notebooks for exploration and documentation
- GitHub for version control
- Streamlit for dashboard creation

### Performance Metric
- Classification accuracy (primary metric)
- Additional metrics: F1-score, precision, recall, and confusion matrix

## Resources

### Dataset Files
- `training_set.csv`: Training data with labels
- `test_set.csv`: Test data for predictions
- `SubmissionFormat.csv`: Template for competition submissions

### Technical Resources
- [Scikit-learn Classification Documentation](https://scikit-learn.org/stable/supervised_learning.html#supervised-learning)
- [GeoPandas Documentation](https://geopandas.org/en/stable/)
- [Folium Documentation](https://python-visualization.github.io/folium/)
- [Streamlit Documentation](https://docs.streamlit.io/)

### Domain Resources
- [Taarifa Platform](https://taarifa.org/)
- [Tanzania Water Point Mapping Project](https://www.maji.go.tz/)


## Audience

* **NGO field teams**: to identify pumps needing urgent repair.
* **Municipal planners**: to allocate resources strategically.
* **Donors & policymakers**: to understand infrastructure reliability and target investments.

## Acknowledgments
- Data provided by Taarifa and the Tanzania Ministry of Water
- Project taken from the DrivenData competition

## License

This project is released under the MIT License. See `LICENSE` for details.

