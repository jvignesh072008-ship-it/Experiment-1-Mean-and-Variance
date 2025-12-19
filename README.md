# Experiment-1-Mean-and-Variance
# Aim: 
To find mean and variance of arrival objects from the feeder using probability distribution.

# Software Required: Python and Visual Components tool

# Theory: 

# 1. Mean (Expectation)

The mean or expected value of a discrete random variable represents its average value, weighted by the probabilities of each possible outcome. It indicates the central tendency or typical value of the variable.
It is calculated as:

<img width="306" height="73" alt="image" src="https://github.com/user-attachments/assets/5f2e0454-bf83-40d8-94f5-7f35b0cda25a" />
										
# 2. Variance
The variance of a random variable measures how much the values of the variable vary from the mean. It shows the spread or dispersion of the data.
It is calculated as:
<img width="998" height="184" alt="image" src="https://github.com/user-attachments/assets/4807d369-afba-4736-b3a4-391effa3dcaf" />


# Algorithm: Mean, Variance, and Standard Deviation of Feeder Arrivals
```






















```
# Program: 
```
Name:Vignesh J

Reg No:25014705

Slot Name: 4J3-1
```

```
import numpy as np 
 
# Input: Enter the number of arrivals separated by space 
L = [int(i) for i in input("Enter arrival data: ").split()] 
 
N = len(L) 
M = max(L) 
x = [] 
f = [] 
 
# Counting frequency of each arrival 
for i in range(M + 1): 
    c = 0 
    for j in range(N): 
        if L[j] == i: 
            c += 1 
    f.append(c) 
    x.append(i) 
 
sf = np.sum(f) 
 
# Calculating probability for each occurrence 
p = [f[i] / sf for i in range(M + 1)] 
 
# Mean of arrival (expected value) 
mean = np.inner(x, p) 
 
# Second moment (E[X²]) 
EX2 = np.inner(np.square(x), p) 
 
# Variance and standard deviation 
var = EX2 - mean**2 
SD = np.sqrt(var) 
 
print(f"The Mean arrival rate is {mean:.3f}") 
print(f"The Variance of arrival from feeder is {var:.3f}") 
print(f"The Standard deviation of arrival from feeder is {SD:.3f}")


```



# Output:
<img width="1268" height="111" alt="Screenshot 2025-11-17 140705" src="https://github.com/user-attachments/assets/1be11d30-3995-46d5-8b60-52009709753c" />




# Result: 
	```
	


	```



