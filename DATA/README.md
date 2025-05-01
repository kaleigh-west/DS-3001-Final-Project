# Obesity Dataset

This folder contains the dataset used for the obesity prediction project.

## Dataset Information
- **Source**: UCI Machine Learning Repository (https://archive.ics.uci.edu/dataset/544/estimation+of+obesity+levels+based+on+eating+habits+and+physical+condition)
- **Name**: Obesity Dataset
- **Size**: 56.3 KB
- **Rows**: 2,111
- **Columns**: 17 (16 features + 1 target)

## Dataset Structure

### Features
1. **Demographic Information**
   - `Gender`: Categorical (Male, Female)
   - `Age`: Numeric (floating/integers)
   - `Height`: Numeric (meters)
   - `Weight`: Numeric (kilograms)

2. **Eating Habits**
   - `family_history_with_overweight`: Categorical (yes, no)
   - `FAVC`: Frequent consumption of high-calorie food (yes, no)
   - `FCVC`: Frequency of consumption of vegetables (Numeric/Ordinal: 1, 2, 3)
   - `NCP`: Number of main meals (Numeric/Ordinal)
   - `CAEC`: Consumption of food between meals (Categorical/Ordinal: Always, Frequently, Sometimes, no)
   - `CH2O`: Daily water intake in liters (Numeric/Ordinal: 1, 2, 3)
   - `SCC`: Monitor calories consumption (yes, no)
   - `CALC`: Consumption of alcohol (Categorical/Ordinal: no, Sometimes, Frequently, Always)

3. **Physical Activity & Lifestyle**
   - `FAF`: Physical activity frequency (Numeric/Ordinal: 0, 1, 2, 3)
   - `TUE`: Time using technology devices (Numeric/Ordinal: 0, 1, 2)
   - `MTRANS`: Transportation used (Categorical: Public_Transportation, Automobile, Walking, Motorbike, Bike)
   - `SMOKE`: Categorical (yes, no)

### Target Variable
- `NObeyesdad`: Multi-class label indicating obesity level
  - Insufficient_Weight
  - Normal_Weight
  - Overweight_Level_I
  - Overweight_Level_II
  - Obesity_Type_I
  - Obesity_Type_II
  - Obesity_Type_III

## Data Preprocessing
The dataset has been preprocessed in the following ways:
- No missing values
- Categorical variables encoded:
  - Binary variables (yes/no) encoded as 1/0
  - Ordinal variables encoded numerically
  - MTRANS one-hot encoded
- Features scaled using StandardScaler and MinMaxScaler

## Data Considerations
1. **Data Quality**
   - Some features rely on self-reporting rather than precise measurements
   - Potential for self-reporting bias in height, weight, and daily intake measurements
   - Important to consider when evaluating model generalizability

2. **Feature Engineering**
   - Most categorical variables are already encoded
   - Some numeric features are effectively ordinal and require careful encoding
   - Consideration needed for class imbalance in the target variable

3. **Modeling Considerations**
   - Target variable has 7 classes
   - Potential need for class balancing techniques
   - Feature importance analysis can reveal key factors in obesity prediction

## Usage
This dataset is used in three different modeling approaches:
1. Unsupervised Learning
2. K-Nearest Neighbors (KNN)
3. Random Forest

## File Format
- Format: CSV
- Encoding: UTF-8 