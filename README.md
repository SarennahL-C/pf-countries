# Country Development Classification — K-Means Clustering Analysis

This project applies **k-means clustering** to group countries based on a range of **socio-economic and health indicators**, with the aim of identifying patterns related to national development status. The analysis explores how variables such as child mortality, income, life expectancy, and GDP per capita interact, and how these relationships can be used to form meaningful clusters.

While the exercise followed a structured notebook template, emphasis was placed on **careful interpretation, validation of clustering choices, and transparent reasoning**, recognising that unsupervised learning does not produce a single “correct” outcome.

![Row of flags of different countries flying outside the United Nations Building in New York](un-flags-common-agenda.jpg)

<sub>Image from https://www.un.org/en/file/127121</sub>

---

## What’s in this repository

- **Jupyter Notebook:** full clustering analysis (`Kmeans_task.ipynb`)  
- **Dataset:** country-level socio-economic data (`Country-data.csv`)  
- **Images:** visualisations of correlations and cluster structure  
- **Requirements:** Python dependencies (`requirements.txt`)  

---

## Project Context

The dataset contains country-level indicators describing economic prosperity, health outcomes, and demographic characteristics. The objective was to use **unsupervised machine learning** to identify natural groupings of countries without predefined labels.

Because clustering does not provide a definitive answer, the analysis focused on:

- Understanding relationships between variables  
- Assessing whether the data was suitable for clustering  
- Selecting an appropriate number of clusters  
- Interpreting clusters in a meaningful socio-economic context  

---

## Approach Overview

The analysis followed a structured exploratory and modelling workflow:

- Exploratory data analysis to understand feature distributions and relationships  
- Correlation analysis and pair plot inspection  
- Feature preparation for k-means clustering  
- Selection of the number of clusters using the **elbow method** and **silhouette scores**  
- Application of k-means clustering  
- Visualisation and interpretation of resulting clusters  

Throughout the process, emphasis was placed on validating assumptions and ensuring interpretability.

---

## Key Insights / Findings

- Strong relationships were observed between key indicators such as child mortality, total fertility rate, income, life expectancy, and GDP per capita.  
- Correlation and pair plot analysis indicated meaningful structure suitable for clustering.  
- Combining elbow and silhouette analyses suggested **k = 3** as the most appropriate balance between separation quality and interpretability.  
- Clusters showed clear differentiation when examined using **GDP per capita** and **child mortality**, which provided the strongest socio-economic meaning.  
- Based on these indicators, clusters were interpreted as representing **developed**, **developing**, and **least developed** countries.  

The analysis reinforced that clustering reveals patterns of similarity rather than definitive classifications.

---

## Skills Demonstrated

**Analysis**
- Exploratory data analysis for unsupervised learning  
- Correlation and pair plot interpretation  
- Feature relationship reasoning  

**Modelling**
- K-means clustering  
- Cluster validation using elbow and silhouette methods  

**Evaluation**
- Interpretation of cluster structure  
- Translation of numerical results into real-world context  

**Tools**
- Python  
- pandas  
- scikit-learn  
- matplotlib / seaborn  
- Jupyter Notebook  

---

## Requirements

Install the required Python packages with: `pip install -r requirements.txt`

---

## Why this project belongs in my portfolio

Clustering problems rarely have a single correct solution, which makes interpretation as important as implementation.

This project demonstrates my ability to evaluate whether clustering is appropriate for a dataset, justify modelling choices, and interpret results thoughtfully rather than mechanically. It complements my supervised learning work by showcasing exploratory pattern discovery and unsupervised machine learning reasoning.
