"""
Standard Deviation Lab
Calculate the standard deviation of books read by learners
Dataset: [1, 5, 6, 6, 8, 13, 14, 18]
"""

import math

# Given dataset
books = [1, 5, 6, 6, 8, 13, 14, 18]
n = 8

print("Standard Deviation Calculation")
print("=" * 40)

# Step 1: Calculate the mean
mean = sum(books) / n
print(f"\nStep 1: Mean = {mean}")

# Step 2: Calculate the squared differences from the mean
print("\nStep 2: Squared differences from the mean:")
squared_diffs = []
for x in books:
    diff = x - mean
    squared = diff ** 2
    squared_diffs.append(squared)
    print(f"({x} - {mean})² = {squared:.2f}")

# Step 3: Calculate the average of these squared differences (variance)
variance = sum(squared_diffs) / n
print(f"\nStep 3: Variance = {variance:.2f}")

# Step 4: Take the square root of the variance to get the standard deviation
std_dev = math.sqrt(variance)
print(f"\nStep 4: Standard Deviation = {std_dev:.2f}")

# Final result
print("\n" + "=" * 40)
print(f"Standard Deviation = {std_dev:.2f}")
print(f"This means that on average, the number of books read by each student")
print(f"deviates from the mean ({mean:.2f}) by {std_dev:.2f} books.")
