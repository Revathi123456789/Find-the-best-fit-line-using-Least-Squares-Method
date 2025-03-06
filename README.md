Implementation of Univariate Linear Regression
AIM:
To implement univariate Linear Regression to fit a straight line using least squares.

Equipments Required:
Hardware – PCs
Anaconda – Python 3.7 Installation / Jupyter notebook
Algorithm
Get the independent variable X and dependent variable Y.
Calculate the mean of the X -values and the mean of the Y -values.
Find the slope m of the line of best fit using the formula.
image

4. Compute the y -intercept of the line by using the formula:
image

5. Use the slope m and the y -intercept to form the equation of the line. 6. Obtain the straight line equation Y=mX+b and plot the scatterplot.
Program:
/*
Program to implement univariate Linear Regression to fit a straight line using least squares.
Developed by: REVATHI K
RegisterNumber:  212223040169

import numpy as np
import matplotlib.pyplot as plt

#preprocessing input data
X=np.array(eval(input()))
Y=np.array(eval(input()))

#mean
X_mean=np.mean(X)
Y_mean=np.mean(Y)
num=0
denom=0

#to find sum of (xi-x') and (yi-y') and (xi-x')^2
for i in range(len(X)):
    num+=(X[i]-X_mean)*(Y[i]-Y_mean)
    denom+=(X[i]-X_mean)**2
    
#calculate slope
m=num/denom

#calculate intercept
b=Y_mean-m*X_mean

print("Slope:{}\nY-intercept:{}".format(m,b))
#line equation
y_predicted=m*X+b
print(y_predicted)

#to plot graph
plt.scatter(X,Y)
plt.plot(X,y_predicted,color='red')
plt.show()
*/
Output:
ml_1

Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.

