# Huffman-Shannon_fano
# Aim:

Consider a discrete memoryless source with symbols and statistics {0.125, 0.0625, 0.25, 0.0625, 0.125, 0.125, 0.25} for its output. Apply the Huffman and Shannon-Fano to this source. Show that draw the tree diagram, the average code word length, Entropy, Variance, Redundancy, Efficiency.

Tools Required:
Python IDE with Numpy and Scipy.

Program:
#Huffman and Shannon-Fano coding
```python
import numpy as np
import math 
L  = 0
hs = 0
p = []
lk = []
n = int(input("Enter the number of Samples : "))
for i in range (n): 
    pr = float(input(f"Enter the probability of sample values {i + 1}: "))  
    p.append(pr)
for j in range (n): 
    l = float(input(f"Enter the length of the sample values {j + 1}: "))  
    lk.append(l)
# Avg length of the code word
for k in range (n):
    Avg1 = p[k] * lk[k]
    L = L + Avg1
# Entropy
for k in range (n):
    e = p[k] * math.log(1 / p[k], 2)
    hs = hs + e
hs = round(hs,3)
# Efficiency
eff =  hs / L
eff = round(eff,3)
# Redundancy 
red =  round(1 - eff,3) 
# Variance
var = 0
for k in range(n):
    var1 = p[k] * (lk[k]-L)**2
    var = var + var1
var = round(var,3)
print(f"Average Codeword Length is : {L}")
print(f"Entropy is : {hs}")
print(f"Efficiency is : {eff}")
print(f"Redudancy is : {red}")
print(f"Variance is : {var}")
```
# Calculation:

<img width="321" height="527" alt="Screenshot 2025-09-29 143355" src="https://github.com/user-attachments/assets/47a12d7b-5e27-4e7a-9ec7-fd749a28bb5f" />

<img width="335" height="209" alt="Screenshot 2025-09-29 143417" src="https://github.com/user-attachments/assets/ce9fa630-32b1-4a17-aa1a-bc441704b5cb" />



# Output:

<img width="666" height="454" alt="Screenshot 2025-09-29 142551" src="https://github.com/user-attachments/assets/dc64111c-3966-4cc9-a792-c27a20d7fa4f" />


# Results:
The Huffman and Shannon-Fano of the given statistics {0.125, 0.0625, 0.25, 0.0625, 0.125, 0.125, 0.25} using python are verified.
