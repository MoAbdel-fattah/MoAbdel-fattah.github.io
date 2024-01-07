---
layout: post
title: Exploring Caesar Cipher Encryption and Decryption
date: 2024-1-07 00:00 +0000
categories: [Python,Cypersecurity]
tags: [python,cypersecurity,cryptography]
---
### Caesar Cipher: A Shifty Affair
- It's a substitution cipher that involves shifting each letter in the plaintext by a fixed number of positions down the alphabet.
- The key determines the shift amount, adding a layer of secrecy to the message.

### Breaking Down the Code:
```python
L2I = dict(zip("ABCDEFGHIJKLMNOPQRSTUVWXYZ", range(26)))
I2L = dict(zip(range(26), "ABCDEFGHIJKLMNOPQRSTUVWXYZ"))
Alpha = "ABCDEFGHIJKLMNOPQRSTUVWXYZ"  # Alphabet for reference
key = 3  # Encryption/decryption key

plaintext = input("Message: ")

ciphertext = ""
for c in plaintext.upper():
    if c.isalpha():
        ciphertext += I2L[(L2I[c] + key) % 26]  # Encryption
    else:
        ciphertext += c

plaintext2 = ""
for c in ciphertext.upper():
    if c.isalpha():
        plaintext2 += I2L[(L2I[c] - key) % 26]  # Decryption
    else:
        plaintext2 += c

print("Ciphertext:", ciphertext)
print("Decrypted Text:", plaintext2)
print("Alphabet:", Alpha)
```
### Key Steps:
- Dictionaries for Letter-Number Mapping: L2I maps letters to numbers, I2L maps numbers to letters.

#### Encryption:
-Each letter in the plaintext is shifted key positions down the alphabet using L2I and I2L.
Non-alphabetical characters are preserved as is.

#### Decryption:
- The ciphertext is decrypted by shifting letters back key positions using L2I and I2L.
Output: The code displays the ciphertext, decrypted text, and the alphabet for reference.

### Key Points:
- The Caesar cipher is a simple example of cryptography, but understanding its mechanism lays a foundation for exploring more complex ciphers.
- It highlights the importance of keys in encryption and decryption processes.
- Python's dictionaries and string manipulation capabilities make implementing such ciphers straightforward.
