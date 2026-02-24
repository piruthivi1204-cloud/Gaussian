# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1.First,we want to import numpy,then import sys,assume a variable.<br>
2.For gaussian elimination method, we want to make 2nd and 3rd column zero.<br>
3.For that we want to make a range accorting to our program output. <br>
4.Then print the program with correct form then the output will display. <br>

## Program:
```python
/*
Program to find the solution of a matrix using Gaussian Elimination.
Developed by: Piruthiviraj G
RegisterNumber: 212225040299
*/
import numpy as np
import sys

n=int(input())
a=np.zeros((n,n+1))
x=np.zeros(n)

for i in range (n):
    for j in range(n+1):
        a[i][j]=float(input())
for i in range(n):        
        if a[i][j]==0.0:
            sys.exit("Divide by zero detected!")
        for j in range(i+1,n):
            ratio=a[j][i]/a[i][i]
            for k in range(n+1):
                a[j][k]=a[j][k]-ratio*a[i][k]
x[n-1]=a[n-1][n]/a[n-1][n-1]
for i in range(n-2,-1,-1):
    x[i]=a[i][n]
    for j in range(i+1,n):
        x[i]=x[i]-a[i][j]*x[j]
        x[i]=x[i]/a[i][i]
for i in range(n):
    print('X%d = %0.2f '%(i,x[i]),end='')
```

## Output:
<img width="1169" height="876" alt="image" src="https://github.com/user-attachments/assets/e81e03df-465a-4b3d-a01c-bdf16d83bb6c" />



## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

