# Data-Analysis

!pip install pandas numpy matplotlib seaborn

import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns

# Load a sample dataset
data = pd.DataFrame({
    'age': np.random.randint(18, 60, size=100),
    'income': np.random.randint(20000, 100000, size=100),
    'education': np.random.choice(['High School', 'Bachelor', 'Master', 'PhD'], size=100)
})

# Descriptive statistics
print("Summary Statistics:")
print(data.describe())

# Visualization: Age distribution
plt.figure(figsize=(8, 6))
sns.histplot(data['age'], kde=True, color='blue')
plt.title('Age Distribution')
plt.xlabel('Age')
plt.ylabel('Frequency')
plt.show()

# Visualization: Income vs Age scatter plot
plt.figure(figsize=(8, 6))
sns.scatterplot(x='age', y='income', data=data, hue='education')
plt.title('Income vs Age')
plt.xlabel('Age')
plt.ylabel('Income')
plt.show()
