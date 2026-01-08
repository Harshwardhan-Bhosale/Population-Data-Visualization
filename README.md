# 📊 Task-01: Data Visualization using Bar Chart

## 🎯 Objective
The objective of this task is to create a bar chart or histogram to visualize the distribution of a categorical or continuous variable, such as the distribution of genders, ages, or continents in a population dataset.

---

## 🌍 Dataset
- **Dataset Used:** World Population Dataset  
- **File Name:** population.csv  
- **Key Column Used:** Continent (Categorical Variable)

---

## 🛠️ Tools & Technologies
- 🐍 Python  
- 🧮 Pandas  
- 📈 Matplotlib  

---

## 📌 Task Description
In this task, a bar chart was created to visualize the distribution of countries across different continents. The dataset was loaded using Pandas, and the frequency of each continent was calculated using value counts. Matplotlib was used to generate a clear and informative bar chart.

---

## 🧪 Implementation

```python
import pandas as pd
import matplotlib.pyplot as plt

# Load dataset
df = pd.read_csv("population.csv")

# Count countries per continent
continent_counts = df["Continent"].value_counts()

# Bar chart
plt.figure(figsize=(8,5))
continent_counts.plot(kind="bar")
plt.title("Distribution of Countries by Continent")
plt.xlabel("Continent")
plt.ylabel("Number of Countries")
plt.xticks(rotation=45)
plt.show()

