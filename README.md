# EX.-NO-2-B-IMPLEMENTATION-OF-RSA

## AIM:
  To write a C program to implement the RSA encryption algorithm.
  
## ALGORITHM:

  STEP-1: Select two co-prime numbers as p and q.
  
  STEP-2: Compute n as the product of p and q.
  
  STEP-3: Compute (p-1)*(q-1) and store it in z.
  
  STEP-4: Select a random prime number e that is less than that of z.
  
  STEP-5: Compute the private key, d as e * mod-1(z).
  
  STEP-6: The cipher text is computed as messagee *
  
  STEP-7: Decryption is done as cipherdmod n.
  
## PROGRAM: 
```
# Python for RSA asymmetric cryptographic algorithm.

import math

def gcd(a, h):
	temp = 0
	while(1):
		temp = a % h
		if (temp == 0):
			return h
		a = h
		h = temp

p = 3
q = 7
n = p*q
e = 2
phi = (p-1)*(q-1)

while (e < phi):
	if(gcd(e, phi) == 1):
		break
	else:
		e = e+1
k = 2
d = (1 + (k*phi))/e

# Message to be encrypted
msg = 12.0

print("Message data = ", msg)

# Encryption c = (msg ^ e) % n
c = pow(msg, e)
c = math.fmod(c, n)
print("Encrypted data = ", c)

# Decryption m = (c ^ d) % n
m = pow(c, d)
m = math.fmod(m, n)
print("Original Message Sent = ", m)
```
## OUTPUT:

![Screenshot 2024-09-25 153422](https://github.com/user-attachments/assets/4f936417-8840-47b7-aaf7-97d9f6969743)

## RESULT:
  Thus the C program to implement RSA encryption technique had been implemented successfully
