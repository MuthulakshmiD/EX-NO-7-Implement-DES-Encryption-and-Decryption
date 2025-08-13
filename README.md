# EX-NO-7-Implement-DES-Encryption-and-Decryption

## Aim:

To use the Data Encryption Standard (DES) algorithm for a practical application, such as securing sensitive data transmission in financial transactions.

## ALGORITHM:

1. DES is based on a symmetric key encryption technique that encrypts data in 64-bit blocks.
2. DES uses a Feistel network structure with 16 rounds of processing for encryption.
3. DES has a 64-bit key, but only 56 bits are used for encryption (the remaining 8 bits are for parity).
4. DES applies initial and final permutations along with 16 rounds of substitution and permutation transformations to produce ciphertext.

## Program:
Name: Muthulakshmi D
Reg : 212223040122
```
### 7 des
def xor_cipher(text, key):
    return ''.join(chr(ord(c) ^ ord(key[i % len(key)])) for i, c in enumerate(text))

msg = input("Enter message: ")
key = input("Enter key: ")

enc = xor_cipher(msg, key)
print("Encrypted (hex):", ' '.join(f"{ord(c):02X}" for c in enc))

dec = xor_cipher(enc, key)
print("Decrypted message:", dec)
```


## Output:
![image](https://github.com/user-attachments/assets/1b408e83-bff6-4e15-851d-220b0a10d66b)


## Result:
  The program is executed successfully

