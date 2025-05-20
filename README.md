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
Python program to implement univariate Linear Regression to fit a straight line using least squares.
#Developed by : SUGESHWA S
#Roll num: 212224230277
'''

import numpy as np
import matplotlib.pyplot as plt
x = np.array([0,1,2,3,4,5,6,7,8,9])
y = np.array([1,3,2,5,7,8,8,9,10,12])
plt.scatter(x,y)
plt.show()
xmean = np.mean(x)
ymean = np.mean(y)
num=0
den=0
for i in range(len(x)):
    num+=(x[i]-xmean)*(y[i]-ymean)
    den+=(x[i]-xmean)**2
m = num/den
b = ymean - m*xmean
print(m,b)
ypred = m*x+b
print(ypred)


plt.scatter(x,y,color='Red')
plt.plot(x,ypred,color='Blue')
plt.show()





```
## Output
![WhatsApp Image 2025-05-20 at 00 23 55_d1bbd2c4](https://github.com/user-attachments/assets/f3688990-617e-41f4-b70a-18a4903c80b6)

![WhatsApp Image 2025-05-20 at 00 23 36_d494bab8](https://github.com/user-attachments/assets/610b6f6a-f3f1-494d-bffc-de052957f14f)


## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
