# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. Read the Argument Matrix.
2. convert it to upper triangular form.
3. Apply back substution to find variables.
4. Display the solution.

## Program:
```
'''Program to solve a matrix using Gaussian elimination without partial pivoting.
Developed by: DEEKSHITHA S
RegisterNumber: 212225100007/25014669
'''
import sys
n = int(input())
A = [[0]*(n+1)for _ in range(n)]
X=[0]*n
for i in range(n):
 for j in range(n+1):
     A[i][j]=float(input())
for i in range(n):
    if A[i][i] == 0.0:
        sys.exit('Divide by zero detected!')
    for j in range(i+1,n):
        r = A[j][i]/A[i][i]
        for k in range(n+1):
            A[j][k]-=r *A[i][k]
X[n-1] = A[n-1][n]/A[n-1][n-1]
for i in range(n-2,-1,-1):
    X[i] = A[i][n]
    for j in range(i+1,n):
        X[i]-= A[i][j]*X[j]
    X[i]/=A[i][i]
    
for i in range(n):
    print('X%d = %0.2f'%(i,X[i]),end=" ")
```

## Output:
<img width="1920" height="1080" alt="Screenshot (114)" src="https://github.com/user-attachments/assets/ff2c003c-d049-4a08-919b-0516789ec92a" />

<img width="1920" height="1080" alt="Screenshot (115)" src="https://github.com/user-attachments/assets/e2c7ca3b-98ac-4ad6-862a-427b29aeeb52" />


## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

