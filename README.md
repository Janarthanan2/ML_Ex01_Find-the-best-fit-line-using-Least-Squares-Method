# Ex01 : Implementation of Univariate Linear Regression
## AIM:
To implement univariate Linear Regression to fit a straight line using least squares.

## EQUIPMENTS REQUIRED:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## ALGORITHM:
1. Get the independent variable X and dependent variable Y.
2. Calculate the mean of the X -values and the mean of the Y -values.
3. Find the slope m of the line of best fit using the formula. 
<img width="231" alt="image" src="https://user-images.githubusercontent.com/93026020/192078527-b3b5ee3e-992f-46c4-865b-3b7ce4ac54ad.png">
4. Compute the y -intercept of the line by using the formula:
<img width="148" alt="image" src="https://user-images.githubusercontent.com/93026020/192078545-79d70b90-7e9d-4b85-9f8b-9d7548a4c5a4.png">
5. Use the slope m and the y -intercept to form the equation of the line.
6. Obtain the straight line equation Y=mX+b and plot the scatterplot.

## PROGRAM:
Program to implement univariate Linear Regression to fit a straight line using least squares.
```
Developed by: JANARTHANAN V K
RegisterNumber:  212222230051
```
```python
## LEAST SQUARE METHOD
import numpy as np
import matplotlib.pyplot as plt

## ASSIGNING INPUT
X=np.array(eval(input()))
Y=np.array(eval(input()))

## MEAN VALUES OF INPUT
X_mean=np.mean(X)
print(X_mean)
Y_mean=np.mean(Y)
print(Y_mean)
num=0
denum=0
for i in range (len(X)):
  num+=(X[i]-X_mean)*(Y[i]-Y_mean)
  denum+=(X[i]-X_mean)**2
  
## FIND THE SLOPE
m=num/denum
print(m)

## FIND THE Y-INTERCEPT
b=Y_mean-m*X_mean
print(b)

## FIND Y_pred
Y_pred=m*X+b
print(Y_pred)

## PLOT GRAPH
plt.scatter(X,Y)
plt.plot(X,Y_pred,color='orange')
plt.show()  
```

## OUTPUT:
    
![244726868-b5ca3fe1-2dc5-4c36-8958-812ce1b3cb1f](https://github.com/Janarthanan2/ML_Ex01_Find-the-best-fit-line-using-Least-Squares-Method/assets/119393515/348e6127-5df4-40f9-b630-721978fc20c1)

    
## RESULT:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
