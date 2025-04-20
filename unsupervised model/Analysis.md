# Unsupervised Learning Analysis for Obesity Dataset

## Introduction

This document presents the results and insights from unsupervised learning techniques applied to the obesity dataset. The analysis employs Principal Component Analysis (PCA) for dimensionality reduction and two clustering algorithms (K-means and Hierarchical Clustering) to identify natural patterns in the data without using the obesity classification labels.

## Methodology

### Dataset Overview
The analysis was performed on a dataset containing various attributes related to eating habits, physical condition, and physical activity that may contribute to obesity. The dataset includes features such as:
- Demographic information (age, gender, height, weight)
- Eating habits (meal frequency, caloric food consumption, water intake)
- Physical activity levels
- Lifestyle factors

### Preprocessing
- Standard scaling was applied to normalize the data
- Categorical variables were encoded appropriately
- Missing values were handled prior to analysis

### Unsupervised Learning Techniques
1. **Principal Component Analysis (PCA)** - Used for:
   - Dimensionality reduction
   - Feature importance analysis
   - Data visualization

2. **K-means Clustering** - Used to:
   - Identify natural groupings in the data
   - Determine optimal number of clusters using:
     - Elbow method
     - Silhouette score

3. **Hierarchical Clustering** - Used to:
   - Validate K-means findings
   - Explore hierarchical relationships between individuals

## Key Findings

### PCA Results
- The PCA analysis determined that approximately 7 principal components are needed to explain 80% of the variance in the data
- This indicates moderate complexity in the dataset that requires multiple dimensions to capture the relationships between variables
- The feature importance analysis from PCA components highlighted the most influential factors in the dataset

### Optimal Clustering
- The elbow method suggested 6 clusters as potentially optimal
- The silhouette score method suggested 10 clusters as optimal
- Based on silhouette score optimization, 10 clusters were selected for the final model, providing more nuanced groupings that better align with the obesity classification patterns

### Cluster Characteristics
The unsupervised analysis revealed 10 distinct clusters with the following characteristics:

**Cluster 0 (11.1% of data)**
- Predominantly insufficient weight individuals (31.6%)
- Low obesity rate (15%)
- Moderate average weight (72.87 kg)
- Higher physical activity (2.25)
- Likely represents active individuals with healthy weight management

**Cluster 1 (9.6% of data)**
- Very high prevalence of Type III obesity (92.1%)
- Extremely high obesity rate (92.6%)
- High average weight (106.33 kg)
- Very low physical activity (0.10)
- Appears to represent individuals with severe obesity and sedentary lifestyle

**Cluster 2 (13.5% of data)**
- Type II obesity dominant (36.7%)
- High obesity rate (63.6%)
- High average weight (100.79 kg)
- Low physical activity (0.73)
- Represents a group with significant obesity and limited physical activity

**Cluster 3 (8.9% of data)**
- Type II obesity dominant (41.0%)
- High obesity rate (59.0%)
- High average weight (100.25 kg)
- Moderate physical activity (1.46)
- Similar to Cluster 2 but with slightly higher physical activity

**Cluster 4 (11.8% of data)**
- Type III obesity dominant (54.8%)
- Extremely high obesity rate (95.2%)
- Very high average weight (127.11 kg)
- Moderate physical activity (1.30)
- Represents individuals with the highest weight but moderate activity level

**Cluster 5 (6.5% of data)**
- Type I obesity dominant (30.4%)
- Moderate obesity rate (50.7%)
- Moderate average weight (81.67 kg)
- Low physical activity (0.67)
- Represents individuals with moderate obesity and limited activity

**Cluster 6 (12.9% of data)**
- Normal weight dominant (32.2%)
- Low obesity rate (11.4%)
- Lower average weight (61.27 kg)
- Moderate physical activity (1.26)
- Represents individuals maintaining normal weight with moderate activity

**Cluster 7 (7.6% of data)**
- Overweight Level I dominant (28.0%)
- Low obesity rate (15.5%)
- Lower average weight (63.29 kg)
- Low physical activity (0.69)
- Represents individuals at risk of obesity with low physical activity

**Cluster 8 (7.0% of data)**
- Type I obesity dominant (39.2%)
- Moderate obesity rate (39.2%)
- Moderate average weight (75.09 kg)
- Low physical activity (0.53)
- Older demographic profile (appears to represent an age-specific obesity pattern)

**Cluster 9 (10.9% of data)**
- Normal weight dominant (25.7%)
- Low obesity rate (14.8%)
- Lower average weight (66.92 kg)
- Low physical activity (0.66)
- Represents individuals maintaining normal weight despite low activity

### Gender Distribution
- Some clusters show strong gender imbalances:
  - Cluster 1: Predominantly female (97%)
  - Cluster 2: Predominantly male (96.9%)
  - Cluster 3: Predominantly male (95.7%)
- This suggests gender-specific obesity risk factors

### Key Discriminating Factors
Based on feature importance analysis, the following factors were most influential in determining cluster membership:

1. **Age (0.8512)** - The most important factor
2. **Number of main meals (NCP) (0.8425)** - Strong influence
3. **Height (0.5682)** and **Weight (0.5461)** - Moderate influence
4. **Physical activity frequency (FAF) (0.5033)** - Moderate influence

Age being the top factor suggests that obesity patterns differ significantly across different age groups.

### Physical Activity and Obesity Relationship
- Clear negative relationship between physical activity and obesity rates across clusters
- Cluster 1 has the lowest physical activity (0.10) and very high obesity rate (92.6%)
- Cluster 0 has the highest physical activity (2.25) and low obesity rate (15%)
- Some exceptions exist (Clusters 7 and 9) where normal/lower weight persists despite low activity

### Categorical Variable Patterns
- Family history with overweight is highly concentrated in obese clusters (95-100%)
- Frequency of consuming high-caloric food (FAVC) shows clear patterns between clusters
- Eating between meals (CAEC) has distinctive patterns across clusters

## Practical Implications

1. **Targeted Interventions**
   - The identified clusters provide a framework for developing targeted obesity prevention and treatment strategies
   - Different approaches should be tailored to the specific characteristics of each group

2. **Risk Identification**
   - The clusters can help identify individuals at risk before they develop obesity
   - Particularly useful for Clusters 7 and 9, which show early warning signs

3. **Physical Activity Focus**
   - The strong relationship between physical activity and obesity across clusters suggests physical activity interventions should be prioritized
   - Specific activity targets could be developed for each cluster

4. **Age-Specific Approaches**
   - With age being the top discriminating factor, interventions should be tailored to different age groups
   - Cluster 8's older demographic requires specific attention

5. **Nutritional Guidance**
   - Meal frequency and dietary habits vary significantly across clusters
   - Nutritional recommendations should consider the cluster-specific patterns

## Conclusion

The unsupervised learning analysis revealed natural groupings in the obesity data that go beyond simple weight classifications. These clusters highlight the complex interplay between physical activity, age, dietary habits, and obesity outcomes. The 10 identified clusters provide a data-driven framework for understanding obesity patterns and developing more personalized prevention and treatment strategies.

The natural alignment between the discovered clusters and obesity levels validates the obesity classification system while adding nuance to our understanding of the different pathways to obesity. This unsupervised approach complements supervised learning methods by identifying patterns without relying on predefined labels, potentially revealing insights that might be missed in supervised approaches. 