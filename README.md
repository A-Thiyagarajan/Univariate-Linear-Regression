# Implementation of Univariate Linear Regression
## Aim:
To implement univariate Linear Regression to fit a straight line using least squares.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
1.	Get the independent variable X and dependent variable Y.
2.	Calculate the mean of the X -values and the mean of the Y -values.
3.	Find the slope m of the line of best fit using the formula.
 ![eqn1](./eq1.jpg)
4.	Compute the y -intercept of the line by using the formula:
![eqn2](./eq2.jpg)  
5.	Use the slope m and the y -intercept to form the equation of the line.
6.	Obtain the straight line equation Y=mX+b and plot the scatterplot.
## Program
```
#Developed by Thiyagarajan A
#Reg.no: 212222240110
import numpy as np
import matplotlib.pyplot as py
x=np.array(eval(input()))
y=np.array(eval(input()))
xbar=np.mean(x)
ybar=np.mean(y)
num,denom=0,0
for i in range(len(x)):
    num+=(x[i]-xbar)*(y[i]-ybar)
    denom+=(x[i]-xbar)**2
m=num/denom
b=ybar-(m*xbar)
print(m,b)
y_pred=(m*x)+b
print(y_pred)
py.scatter(x,y,color="green")
py.plot(x,y_pred,color="red")
py.show()
```
## Output
![10](https://github.com/A-Thiyagarajan/Univariate-Linear-Regression/assets/118707693/972264a4-9c7f-4391-85c6-68da15c86f6d)



## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
