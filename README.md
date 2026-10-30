# Implementation of Univariate Linear Regression

## AIM:
To implement univariate Linear Regression to fit a straight line using least squares.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Get the independent variable X and dependent variable Y.
2. Calculate the mean of the X-values and the mean of the Y-values.
3. Find the slope m of the line of best fit using the formula:
   m = Σ(Xi − X̄)(Yi − Ȳ) / Σ(Xi − X̄)²
4. Compute the y-intercept of the line by using the formula:
   b = Ȳ − m·X̄
5. Use the slope m and the y-intercept b to form the equation of the line.
6. Obtain the straight line equation Y = mX + b and plot the scatterplot.

## Program:
```python
'''
Program to implement univariate Linear Regression to fit a straight line using least squares.
Developed by: <S.DURGESH>
RegisterNumber: <212225230064>
'''
import numpy as np
import matplotlib.pyplot as plt


X = np.array([1, 2, 3, 4, 5])
Y = np.array([2, 4, 5, 4, 5])


x_mean = np.mean(X)
y_mean = np.mean(Y)


m = np.sum((X - x_mean) * (Y - y_mean)) / np.sum((X - x_mean) ** 2)

b = y_mean - m * x_mean


print("Slope (m) =", m)
print("Intercept (b) =", b)
print(f"Equation of the line: Y = {m}X + {b}")


Y_pred = m * X + b
plt.scatter(X, Y, color="blue", label="Data points")
plt.plot(X, Y_pred, color="red", label="Best fit line")
plt.xlabel("X")
plt.ylabel("Y")
plt.title("Univariate Linear Regression (Least Squares)")
plt.legend()
plt.show()
```

## Output:
```
Slope (m) = 0.6
Intercept (b) = 2.2
Equation of the line: Y = 0.6X + 2.2
```
<img width="748" height="565" alt="image" src="https://github.com/user-attachments/assets/a3cf7853-2cff-4314-ad6f-7d1387a81135" />



## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
