# PROGRAMMING ASSIGNMENT 2
##### GREFALDEO, Lettice Hyacinth | 2ECE-C

This repository contains Python scripts designed to solve the different problems given in ECE 2112, Programming Assignment 1. Below is a summary of each script

### Problem 1 - Reproducible Normalization Problem
###### This problem will be creating a 5x5 array with random integers and will be normalized using the given formula.

```python
import numpy as np

np.random.seed(2112)
X = np.random.randint(10, 101, size=(5,5)) #create a 5x5 size array 

#state the variables needed to normalize the array 
Xmean = np.mean(X)
Xstd = np.std(X)

#normalize using the given formula 
X_normalized = (X-Xmean)/(Xstd)

#display necessary output 
print("X:\n", X)
print("\nX_normalized:\n", X_normalized)
print("\nMean:", np.mean(X_normalized))
print("Standard Deviation:", np.std(X_normalized))

#save
np.save("X_normalized.npy", X_normalized)
```

**Output:**

<img width="805" height="342" alt="image" src="https://github.com/user-attachments/assets/900a59d4-d6dd-43d4-9259-ec1fc40157ec" />


### Problem 2 - Cubes Divisible by 4 Problem
###### This problem will create a 10x10 array and will cube each element while filtering elements that are divisible by 4, those elements will be shown in the resulting array 

```python
import numpy as np 

#create a 10x10 array
ndarray = np.arange(1, 101)

#cube each element of the array
C = ndarray**3
C = C.reshape(10, 10)
div_by_4 = C[C % 4 == 0] #filter the elements divisible by 4

#display the necessary output
print("Shape of C:", C.shape)
print("\nValues divisible by 4:\n", div_by_4)
print("\nNumber of elements:", div_by_4.size)

#save
np.save("div_by_4.npy", div_by_4)
```

**Output:**

<img width="1008" height="237" alt="image" src="https://github.com/user-attachments/assets/dab61155-8188-412f-bd43-27c588c038c7" />


### Problem 3 - Above-Mean Sqaures Problem
###### This problem creates a 6x6 array with positive integers only. This then computes the mean of the array and displays a new array showing the values that are above the mean from the original array. 

```python
import numpy as np

#create a 6x6 array named S, with positive integers only
S = np.arange(1,37)**2 #for positive integers only
S = S.reshape(6,6)

#compute mean
S_mean = np.mean(S)

#filter the elements that it is above the mean
above_mean = S[S>S_mean]

#display the necessary output
print("S:\n", S)
print("\nMean:", S_mean)
print("\nAbove mean:\n", above_mean)
print("\nNumber of elements:", above_mean.size) #first element should be 484, last element should be 1296

#save the file
np.save("above_mean.npy", above_mean)
```

**Output:**

<img width="1101" height="322" alt="image" src="https://github.com/user-attachments/assets/49c800bf-b747-4d09-aee0-a46a8ce21109" />











