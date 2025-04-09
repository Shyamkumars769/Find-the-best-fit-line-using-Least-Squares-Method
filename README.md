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
/*
Program to implement univariate Linear Regression to fit a straight line using least squares.
Developed by:shyam kumar
RegisterNumber: 212224040315
*/
```
```
import numpy as np
import matplotlib.pyplot as plt
print("Enter X values: ")
X = [float(i) for i in input().split()]
X = np.array(X)
print("Enter Y values: ")
Y = [float(i) for i in input().split()]
print("--------------------------------")
Y = np.array(Y)
X_mean = np.mean(X)
Y_mean = np.mean(Y)
print("Mean of X: ",X_mean)
print("Mean of Y: ",Y_mean)
num = 0
denum = 0
for i in range(len(X)):
    num = num + ((X[i] - X_mean)*(Y[i] - Y_mean))
    denum = denum + ((X[i]-X_mean)**2)
m = num/denum
print("Slope: ",m)

b = (Y_mean - (m*X_mean))
print("Y intercept: ",b)
Y_line = m*X + b
print("Y Line: ",Y_line)
plt.scatter(X,Y)
plt.plot(X,Y_line)
plt.show()
```
## Output:
![image](https://github.com/user-attachments/assets/98619fcb-49ed-4705-a3c1-c599269ff271)
![image](https://github.com/user-attachments/assets/e7c6bcda-8a5d-4d5b-90f1-d3d0ce53ac8e)


## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
