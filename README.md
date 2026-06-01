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


## Algorithm
1. Import the NumPy library and define the matrix A.
2. Initialize the lower triangular matrix L and upper triangular matrix U with zeros.
3. Compute the elements of U row by row.
4. Compute the elements of L column by column and set the diagonal elements of L to 1.
5. Display matrices L and U, and verify that A=LU.

## Program:
(i) To find the L and U matrix
```

'''Program to find L and U matrix using LU decomposition.
Developed by: ASHLEY ANTONY
RegisterNumber: 212225220013
'''
import os
os.environ["OPENBLAS_NUM_THREADS"]="1"
import numpy as np 
from scipy.linalg import lu
matrix = np.array(eval(input()))
P,L,U=lu(matrix)
print(L)
print(U)


```
(ii) To find the LU Decomposition of a matrix
```
'''Program to solve a matrix using LU decomposition.
Developed by: ASHLEY ANTONY
RegisterNumber: 212225220013
'''
import os
os.environ["OPENBLAS_NUM_THREADS"]="1"
# To print X matrix (solution to the equations)
import numpy as np
from scipy.linalg import lu_factor,lu_solve
A=np.array(eval(input()))
B=np.array(eval(input()))
lu,pivot=lu_factor(A)
x=lu_solve((lu,pivot),B)
print(x)
```

## Output:

<img width="994" height="388" alt="WhatsApp Image 2026-06-01 at 9 37 21 AM" src="https://github.com/user-attachments/assets/689e5743-2b4a-4529-871e-abdc1b25043c" />




<img width="1035" height="166" alt="WhatsApp Image 2026-06-01 at 9 37 48 AM" src="https://github.com/user-attachments/assets/de6309a9-5669-40dd-8e6f-8989103fed68" />

## Result:
Thus the program to find the LU Decomposition of a matrix is written and verified using python programming.

