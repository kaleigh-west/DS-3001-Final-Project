# Obesity Level Prediction Project

## Project Overview
This project aims to predict obesity levels based on eating habits and physical condition using various machine learning approaches. The analysis includes both supervised (KNN and Random Forest) and unsupervised learning methods to understand patterns and predict obesity levels.

## Team Members
- Alice Chang
- Aymen Zouari
- Blake Richardson
- Kaleigh West
- Ryder Robins

## Project Structure
```
.
├── DATA/
│   ├── ObesityDataSet_raw_and_data_sinthetic.csv
│   └── README.md
├── KNN model/
│   ├── SCRIPT/
│   ├── OUTPUT/
│   └── Analysis.md
├── Random Forest model/
│   ├── SCRIPT/
│   ├── OUTPUT/
│   └── Analysis.md
├── unsupervised model/
│   ├── SCRIPT/
│   ├── OUTPUT/
│   └── Analysis.md
├── EDA.ipynb
└── README.md
```

## Methodology

### 1. Exploratory Data Analysis (EDA)
- Initial data exploration and visualization
- Feature analysis and correlation studies
- Data preprocessing insights

### 2. Supervised Learning Approaches

#### K-Nearest Neighbors (KNN)
- Binary classification approach
- Hyperparameter tuning through grid search
- Cross-validation for robust evaluation
- Performance metrics and visualization

#### Random Forest
- Ensemble learning approach
- Feature importance analysis
- Hyperparameter optimization
- Model performance evaluation

### 3. Unsupervised Learning
- Clustering analysis
- Pattern discovery
- Feature relationship exploration

## Key Findings
- Identification of significant predictors of obesity
- Comparison of different modeling approaches
- Insights into feature importance
- Model performance metrics and visualizations

## Getting Started

### Prerequisites
- Python 3.x
- Required Python packages (list in requirements.txt)
- Jupyter Notebook

### Installation
1. Clone the repository
2. Install required packages:
   ```bash
   pip install -r requirements.txt
   ```

### Usage
1. Start with `EDA.ipynb` for initial data exploration
2. Navigate to specific model folders for detailed analysis:
   - KNN model/
   - Random Forest model/
   - unsupervised model/

## Results
Detailed results and analysis can be found in each model's respective folder:
- Model performance metrics
- Feature importance analysis
- Visualization of results
- Comparative analysis

## Future Work
- Further model optimization
- Additional feature engineering
- Integration with healthcare systems
- Real-time prediction capability

## License
This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments
- UCI Machine Learning Repository for the dataset
- Contributors and team members
- Course instructors and mentors
