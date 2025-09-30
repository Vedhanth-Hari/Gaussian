# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm:
# step-1:
Import numpy and define the matrix with coefficient and constants 
# step-2:
Convert the matrix to an upper triangular matrix 
# step-3:
Solve for variables starting from the last row and print 
# step-4:
End the program
 

## Program:
```
/*
'''Program to solve a matrix using Gaussian elimination without partial pivoting.
Developed by: H.Vedhanth
RegisterNumber: 212224240181
*/
import numpy as np
import sys
n=int(input())
a=np.zeros((n,n+1))
x=np.zeros(n)
for i in range(n):
    for j in range(n+1):
        a[i][j]=float(input())
for i in range(n):
    if a[i][i]==0.0:
        sys.exit('Divide by zero detected!');
    for j in range(i+1,n):
        ratio=a[j][i]/a[i][i]
        for k in range(n+1):
            a[j][k]=a[j][k]-ratio*a[i][k]
x[n-1]=a[n-1][n]/a[n-1][n-1]
for i in range(n-2,-1,-1):
    x[i]=a[i][n]
    for j in range(n-2,-1,-1):
        x[i]=a[i][n]
        for j in range(i+1,n):
            x[i]=x[i]-a[i][j]*x[j]
        x[i]=x[i]/a[i][i]
for i in range(n):
    print('X%d = %0.2f' %(i,x[i]),end = ' ')
```

## Output:
![gaussian elimination]()


<img width="1424" height="980" alt="Screenshot 2025-09-30 135213" src="https://github.com/user-attachments/assets/51ecf19c-1d9b-435a-8f87-9260b70555b4" />
<img width="1437" height="974" alt="Screenshot 2025-09-30 135255" src="https://github.com/user-attachments/assets/d84283de-3940-4538-b3b1-d663b69db23d" />


## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

