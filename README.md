# Implementation of Univariate Linear Regression
## AIM:
To implement univariate Linear Regression to fit a straight line using least squares.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Get the independent variable X and dependent variable Y.
2. Calculate the mean of the X -values and the mean of the Y -values.
3. Find the slope m of the line of best fit using the formula. 
<img width="231" alt="image" src="https://user-images.githubusercontent.com/93026020/192078527-b3b5ee3e-992f-46c4-865b-3b7ce4ac54ad.png">
4. Compute the y -intercept of the line by using the formula:
<img width="148" alt="image" src="https://user-images.githubusercontent.com/93026020/192078545-79d70b90-7e9d-4b85-9f8b-9d7548a4c5a4.png">
5. Use the slope m and the y -intercept to form the equation of the line.
6. Obtain the straight line equation Y=mX+b and plot the scatterplot.

## Program:
```
Program to implement univariate Linear Regression to fit a straight line using least squares.
Developed by: Abdul Rasak . N 
RegisterNumber:  24002896


import numpy as np
import matplotlib.pyplot as plt

# Input the data as numpy arrays
X = np.array(eval(input("Enter the X values as a list: ")))
Y = np.array(eval(input("Enter the Y values as a list: ")))

# Calculate the mean of X and Y
X_mean = np.mean(X)
Y_mean = np.mean(Y)

# Initialize numerator and denominator for calculating slope
num = 0
denom = 0

# Calculate the slope (m) using the formula
for i in range(len(X)):
    num += (X[i] - X_mean) * (Y[i] - Y_mean)
    denom += (X[i] - X_mean) ** 2

m = num / denom

# Calculate the intercept (b)
b = Y_mean - m * X_mean

# Print the slope and intercept
print(f"Slope (m): {m}")
print(f"Intercept (b): {b}")

# Predicted Y values based on the regression line
Y_predicted = m * X + b

# Print the predicted Y values
print("Predicted Y values: ", Y_predicted)

# Plot the original data points and the regression line
plt.scatter(X, Y, color='blue', label='Original Data')
plt.plot(X, Y_predicted, color='red', label='Regression Line')

# Add labels and legend
plt.xlabel('X')
plt.ylabel('Y')
plt.legend()

# Show the plot
plt.show()
```

## Output:
![image](https://github.com/user-attachments/assets/9954a148-9620-4694-848e-2565f781922b)



## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
