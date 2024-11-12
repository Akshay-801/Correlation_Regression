# Correlation and regression for data analysis
# Aim : 

To analyse given data using coeffificient of correlation and regression line
![image](https://user-images.githubusercontent.com/104613195/168224136-d6b64e64-7d3d-4775-9337-c8f96fe41f2d.png)


# Software required :  

Python

# Theory:

Correlation describes the strength of an association between two variables, and is completely symmetrical, the correlation between A and B is the same as the correlation between B and A. However, if the two variables are related it means that when one changes by a certain amount the other changes on an average by a certain amount.  

If y represents the dependent variable and x the independent variable, this relationship is described as the regression of y on x. The relationship can be represented by a simple equation called the regression equation. The regression equation representing how much y changes with any given change of x can be used to construct a regression line on a scatter diagram, and in the simplest case this is assumed to be a straight line.

# Procedure :

![image](https://user-images.githubusercontent.com/104613195/168225866-ac8f6610-bdc3-4ac2-a24e-2b24ba08e189.png)

# Program :

```
import numpy as np
import matplotlib.pyplot as plt
import math
x=[int(i) for i in input().split()]
y=[int(i) for i in input().split()]
n=len(x)
sx=sy=sxy=sx2=sy2=0
for i in range(n):
    sx+=x[i]
    sy+=y[i]
    sxy+=x[i]*y[i]
    sx2+=x[i]*x[i]
    sy2+=y[i]*y[i]
r=((n*sxy)-(sx*sy))/(math.sqrt(n*sx2-(sx*sx))*math.sqrt(n*sy2-(sy*sy)))
print("The coorelation coefficient is %0.3f"%r)
byx=(n*sxy-sx*sy)/(n*sx2-sx**2)
xmean=sx/n
ymean=sy/n
print('The regression line Y on X is Y = %0.3f %0.3f (x-%0.3f)'%(ymean,byx,xmean))
plt.scatter(x,y)
def reg(x):
    return ymean+byx*(x-xmean)
x=np.linspace(0,80,51)
y1=reg(x)
plt.plot(x,y1,'r')
plt.xlabel('x-data')
plt.ylabel('y-data')
plt.legend(['data points','regression line'])
plt.show()

```

# Output

<img src="https://github.com/user-attachments/assets/4530d7a2-cfa9-4bb4-aad4-07f3bfcc0ce0"  width="400" />
<br>
<img src="https://github.com/user-attachments/assets/8e69ab0c-a17d-4209-9aef-f1c28a6a20d5" width="400" />


# Result 

The given data is analysed using coeffificient of correlation and regression line.

