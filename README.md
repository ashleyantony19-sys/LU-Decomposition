# LU Decomposition 

## AIM:
To write a program to find the LU Decomposition of a matrix.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. Read the matrix from the user.
2. Initialize lower triangular matrix L and upper triangular matrix U.
3. Compute the elements of U matrix.
4. Compute the elements of L matrix.
5. Display the matrices L and U.
6. Verify that A = LU.

## Program:
(i) To find the L and U matrix
```

Program to find the L and U matrix.
Developed by: Ashley Antony
RegisterNumber: 212225220013

import numpy as np

A = np.array([[2, -1, -2],
              [-4, 6, 3],
              [-4, -2, 8]], dtype=float)

n = len(A)

L = np.zeros((n, n))
U = np.zeros((n, n))

for i in range(n):

    # Upper Triangular Matrix
    for k in range(i, n):
        sum = 0
        for j in range(i):
            sum += (L[i][j] * U[j][k])

        U[i][k] = A[i][k] - sum

    # Lower Triangular Matrix
    L[i][i] = 1

    for k in range(i + 1, n):
        sum = 0
        for j in range(i):
            sum += (L[k][j] * U[j][i])

        L[k][i] = (A[k][i] - sum) / U[i][i]

print("Lower Triangular Matrix L:")
print(L)

print("\nUpper Triangular Matrix U:")
print(U)
```
(ii) To find the LU Decomposition of a matrix
```

Program to find the LU Decomposition of a matrix.
Developed by: 
RegisterNumber: 


import numpy as np
A = np.array([[2, -1, -2],
              [-4, 6, 3],
                [-4, -2, 8]], dtype=float)
 n = len(A)
 L = np.zeros((n, n))
 U = np.zeros((n, n))
for i in range(n):
  for k in range(i, n):
    total = 0
      for j in range(i):
            total += L[i][j] * U[j][k]
            U[i][k] = A[i][k] - total
            L[i][i] = 1
for k in range(i + 1, n):
    total = 0
for j in range(i):
    total += L[k][j] * U[j][i] L[k][i] = (A[k][i] - total) / U[i][i]
print("Matrix A:")
print(A)
print("\nLower Matrix L:")
print(L)
print("\nUpper Matrix U:")
print(U)
print("\nLU Decomposition:")
print(np.dot(L, U))
```

## Output:


<img width="377" height="363" alt="image" src="https://github.com/user-attachments/assets/46be8c74-d862-415f-968b-e5f1781f0064" />



## Result:
Thus the program to find the LU Decomposition of a matrix is written and verified using python programming.

