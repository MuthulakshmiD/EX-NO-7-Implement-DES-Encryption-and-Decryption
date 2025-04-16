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
def encrypt(message, key):
    encrypted = []
    key_length = len(key)
    for i in range(len(message)):
        encrypted_char = chr(ord(message[i]) ^ ord(key[i % key_length]))
        encrypted.append(encrypted_char)
    return ''.join(encrypted)

def decrypt(encrypted_message, key):
    # XOR again with the same key
    decrypted = []
    key_length = len(key)
    for i in range(len(encrypted_message)):
        decrypted_char = chr(ord(encrypted_message[i]) ^ ord(key[i % key_length]))
        decrypted.append(decrypted_char)
    return ''.join(decrypted)

# Main simulation
print("\n***** Simulation of XOR Encryption and Decryption *****\n")

# Get user input
message = input("Enter the message to encrypt: ")
key = input("Enter the encryption key: ")

# Encrypt
encrypted_message = encrypt(message, key)

# Show original and encrypted message
print("\nOriginal Message:", message)
print("Encrypted Message (in hex):", ' '.join(f"{ord(c):02X}" for c in encrypted_message))

# Decrypt
decrypted_message = decrypt(encrypted_message, key)
print("Decrypted Message:", decrypted_message)
```


## Output:
![image](https://github.com/user-attachments/assets/1b408e83-bff6-4e15-851d-220b0a10d66b)


## Result:
  The program is executed successfully

