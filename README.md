# Country Development Classification — K-Means Clustering Analysis

This project applies **k-means clustering** to group countries based on a range of **socio-economic and health indicators**, with the aim of identifying patterns related to national development status.

The analysis explores how variables such as child mortality, income, life expectancy, and GDP per capita interact, and how these relationships can be used to group countries into meaningful clusters. While the exercise followed a structured notebook template, emphasis was placed on **careful interpretation, validation of clustering choices, and transparent reasoning**.

![Row of flags of different countries flying outside the United Nations Building in New York](un-flags-common-agenda.jpg)

Image from https://www.un.org/en/file/127121

### What’s in this repository

- **Jupyter Notebook:** step-by-step analysis (`Kmeans_task.ipynb`)    
- **Images:** visuals
- **Source data:** csv dataset (`Country-data.csv`)  
- **Requirements:** Python dependencies (`requirements.txt`)

---

### Project Context

The dataset contains country-level indicators describing economic prosperity, health outcomes, and demographic characteristics. The goal of the task was to use **unsupervised machine learning** to identify natural groupings of countries without predefined labels.

Because clustering does not provide a “correct answer,” the analysis focused on:

- Understanding relationships between variables  
- Selecting an appropriate number of clusters  
- Interpreting clusters in a meaningful, real-world context  

---

### Exploratory Data Analysis

Before clustering, exploratory analysis was used to understand feature relationships and suitability for k-means.

#### Correlation Analysis

A correlation heatmap revealed several strong relationships:

**Strong positive correlations**
- Child mortality and total fertility rate  
- Exports with imports and income  
- Income with GDP per capita  
- Life expectancy with GDP per capita  

These relationships indicate that:
- Higher child mortality is associated with larger family sizes  
- Increased national prosperity corresponds with greater trade activity and income  
- Life expectancy rises alongside income and GDP per person  

**Strong negative correlations**
- Child mortality with life expectancy and income  
- Income with total fertility rate  
- Life expectancy with total fertility rate  

These patterns suggest that:
- Countries with high child mortality tend to have lower income and shorter life expectancy  
- Lower income and life expectancy are associated with larger family sizes  

Imports and inflation showed relatively weak relationships with other variables.

---

#### Pair Plot Analysis

Pair plots were used to further explore feature relationships prior to clustering.

Key patterns observed included:

**Positive relationships**
- Total fertility rate and child mortality  
- GDP per capita and income  

**Negative relationships**
- Child mortality and life expectancy  
- Total fertility rate and life expectancy  

These relationships supported the expectation that the dataset contains meaningful structure suitable for clustering.

---

## Preparing for K-Means Clustering

Because k-means requires the number of clusters to be defined in advance, two methods were used to guide selection:

- **Elbow method**
- **Silhouette score analysis**

The elbow curve suggested a reasonable range between **3 and 6 clusters**, while silhouette scores were considerably higher for **k = 2 and k = 3**. Considering both results together, **k = 3** was selected as the most appropriate balance between separation quality and interpretability.

---

### Clustering Results and Interpretation

K-means clustering was performed using **k = 3**, and the resulting clusters were visualised across multiple feature combinations.

![Two scatter plots side by side. The left one shows child mortality as a function of gdp per capita and the right one shows inflation as a function of gdp per capita. The data points are colored by country development status,as identified in the analysis. There is minimal overlap between the statuses.](k-means-clusters.png)

Cluster interpretation was based primarily on:

- **GDP per capita (gdpp)**
- **Child mortality**

These two variables provided the clearest separation and strongest socio-economic meaning.

Based on these indicators, the clusters were labelled as:

- **Cluster 0 — Developing countries**  
- **Cluster 1 — Developed countries**  
- **Cluster 2 — Least developed countries**

Countries in the developed cluster exhibited high GDP per capita and low child mortality, while the least developed cluster showed the opposite pattern. The developing cluster fell between these two extremes.

Final visualisations included labelled clusters and a summary table listing all countries assigned to each group.

---

### Skills Demonstrated

- Exploratory data analysis for unsupervised learning  
- Correlation and pair plot interpretation  
- Feature relationship reasoning  
- K-means clustering  
- Cluster validation (elbow method and silhouette score)  
- Translating numerical clusters into meaningful real-world categories  
- Python data science tools: pandas, scikit-learn, matplotlib, seaborn  

---

### Requirements

Install the required Python dependencies with: `pip install -r requirements.txt`

---

### Why this project belongs in my portfolio

Clustering problems rarely have a single correct solution, which makes interpretation as important as implementation.

This project demonstrates my ability to:
- evaluate whether clustering is appropriate for a dataset
- justify the choice of the number of clusters
- interpret results thoughtfully rather than mechanically
- connect statistical patterns to meaningful real-world context

It complements my supervised learning projects by showcasing my understanding of unsupervised machine learning and exploratory pattern discovery.


