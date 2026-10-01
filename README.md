# ================================================================
# DATA VISUALIZATION ASSIGNMENT
# MATPLOTLIB + SEABORN + PLOTLY + BOKEH
# ================================================================


# ================================================================
# PART A: MATPLOTLIB ASSIGNMENT
# ================================================================

# Q1. Create a scatter plot using Matplotlib to visualize the
# relationship between two arrays, x and y for the given data.
#
# Given Data:
# x = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
# y = [2, 4, 5, 7, 6, 8, 9, 10, 12, 13]

import matplotlib.pyplot as plt

x = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
y = [2, 4, 5, 7, 6, 8, 9, 10, 12, 13]

plt.figure(figsize=(8, 5))
plt.scatter(x, y)

plt.title("Scatter Plot of X and Y")
plt.xlabel("X Values")
plt.ylabel("Y Values")
plt.grid(True)

plt.show()


# ----------------------------------------------------------------

# Q2. Generate a line plot to visualize the trend of values
# for the given data.
#
# Given Data:
# data = np.array([3, 7, 9, 15, 22, 29, 35])

import numpy as np
import matplotlib.pyplot as plt

data = np.array([3, 7, 9, 15, 22, 29, 35])

plt.figure(figsize=(8, 5))
plt.plot(data, marker='o')

plt.title("Line Plot Showing Trend of Values")
plt.xlabel("Index")
plt.ylabel("Values")
plt.grid(True)

plt.show()


# ----------------------------------------------------------------

# Q3. Display a bar chart to represent the frequency of each item
# in the given array categories.
#
# Given Data:
# categories = ['A', 'B', 'C', 'D', 'E']
# values = [25, 40, 30, 35, 20]

import matplotlib.pyplot as plt

categories = ['A', 'B', 'C', 'D', 'E']
values = [25, 40, 30, 35, 20]

plt.figure(figsize=(8, 5))
plt.bar(categories, values)

plt.title("Frequency of Each Category")
plt.xlabel("Categories")
plt.ylabel("Frequency")
plt.grid(axis='y')

plt.show()


# ----------------------------------------------------------------

# Q4. Create a histogram to visualize the distribution of values
# in the array data.
#
# Given Data:
# data = np.random.normal(0, 1, 1000)

import numpy as np
import matplotlib.pyplot as plt

data = np.random.normal(0, 1, 1000)

plt.figure(figsize=(8, 5))
plt.hist(data, bins=30)

plt.title("Distribution of Data")
plt.xlabel("Values")
plt.ylabel("Frequency")
plt.grid(axis='y')

plt.show()


# ----------------------------------------------------------------

# Q5. Show a pie chart to represent the percentage distribution
# of different sections in the array 'sections'.
#
# Given Data:
# sections = ['Section A', 'Section B', 'Section C', 'Section D']
# sizes = [25, 30, 15, 30]

import matplotlib.pyplot as plt

sections = ['Section A', 'Section B', 'Section C', 'Section D']
sizes = [25, 30, 15, 30]

plt.figure(figsize=(7, 7))
plt.pie(
    sizes,
    labels=sections,
    autopct='%1.1f%%',
    startangle=90
)

plt.title("Percentage Distribution of Sections")
plt.show()



# ================================================================
# PART B: SEABORN ASSIGNMENT
# ================================================================

# Q1. Create a scatter plot to visualize the relationship between
# two variables, by generating a synthetic dataset.

import numpy as np
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt

np.random.seed(10)

data = {
    'X': np.random.rand(100) * 100,
    'Y': np.random.rand(100) * 100
}

df = pd.DataFrame(data)

plt.figure(figsize=(8, 5))
sns.scatterplot(data=df, x='X', y='Y')

plt.title("Scatter Plot of Synthetic Dataset")
plt.xlabel("X")
plt.ylabel("Y")

plt.show()


# ----------------------------------------------------------------

# Q2. Generate a dataset of random numbers. Visualize the
# distribution of a numerical variable.

import numpy as np
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt

np.random.seed(10)

data = {
    'Values': np.random.randn(1000)
}

df = pd.DataFrame(data)

plt.figure(figsize=(8, 5))
sns.histplot(data=df, x='Values', bins=30, kde=True)

plt.title("Distribution of Random Numerical Values")
plt.xlabel("Values")
plt.ylabel("Frequency")

plt.show()


# ----------------------------------------------------------------

# Q3. Create a dataset representing categories and their
# corresponding values. Compare different categories based
# on numerical values.

import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt

data = {
    'Category': ['A', 'B', 'C', 'D', 'E'],
    'Value': [25, 40, 30, 35, 20]
}

df = pd.DataFrame(data)

plt.figure(figsize=(8, 5))
sns.barplot(data=df, x='Category', y='Value')

plt.title("Comparison of Different Categories")
plt.xlabel("Category")
plt.ylabel("Value")

plt.show()


# ----------------------------------------------------------------

# Q4.
