# Import necessary libraries
import numpy as np
import matplotlib.pyplot as plt

# Step 1: Generate random data
# Create an array of 1000 random numbers following a normal distribution (mean=50, std=10)
data = np.random.normal(loc=50, scale=10, size=1000)

# Step 2: Perform basic statistical analysis
mean = np.mean(data)
median = np.median(data)
std_dev = np.std(data)

# Step 3: Output the results
print(f"Mean of the data: {mean:.2f}")
print(f"Median of the data: {median:.2f}")
print(f"Standard Deviation of the data: {std_dev:.2f}")

# Step 4: Visualize the data

# Histogram: To show the distribution of the data
plt.figure(figsize=(10, 6))
plt.hist(data, bins=30, edgecolor='black', alpha=0.7)
plt.title('Histogram of Random Data')
plt.xlabel('Value')
plt.ylabel('Frequency')
plt.grid(True)
plt.show()

# Line plot: Showing the cumulative sum of the data
cumsum_data = np.cumsum(data)
plt.figure(figsize=(10, 6))
plt.plot(cumsum_data, color='blue', label='Cumulative Sum')
plt.title('Cumulative Sum of Random Data')
plt.xlabel('Index')
plt.ylabel('Cumulative Sum')
plt.legend()
plt.grid(True)
plt.show()
