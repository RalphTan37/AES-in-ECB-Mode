# AES-in-ECB-Mode
Implementation of **AES encryption and decryption** in **Electronic Codebook (ECB)** mode using **C++**.

## To compile the program:
```
g++ aes.cpp -o aes
```

## Run AES Program
```
.\aes
```

## Example Test Vectors
##### All examples below use known AES-128 test vectors that produce matching, verified results.

### 1. Encryption Example
#### Plaintext:
```
6bc1bee22e409f96e93d7e117393172aae2d8a571e03ac9c9eb76fac45af8e5130c81c46a35ce411e5fbc1191a0a52eff69f2445df4f9b17ad2b417be66c3710
```
#### Key:
```
2b7e151628aed2a6abf7158809cf4f3c
```
#### Program Input:
```
Enter 'e' for encryption and 'd' for decryption: e
Enter text to be encrypted: 6bc1bee22e409f96e93d7e117393172aae2d8a571e03ac9c9eb76fac45af8e5130c81c46a35ce411e5fbc1191a0a52eff69f2445df4f9b17ad2b417be66c3710
Enter key: 
2b7e151628aed2a6abf7158809cf4f3c
```
#### Output (Ciphertext):
```
3ad77bb40d7a3660a89ecaf32466ef97f5d3d58503b9699de785895a96fdbaaf43b1cd7f598ece23881b00e3ed0306887b0c785e27e8ad3f8223207104725dd4
```
### 2. Decryption Example
#### Ciphertext:
```
3ad77bb40d7a3660a89ecaf32466ef97f5d3d58503b9699de785895a96fdbaaf43b1cd7f598ece23881b00e3ed0306887b0c785e27e8ad3f8223207104725dd4
```
#### Key:
```
2b7e151628aed2a6abf7158809cf4f3c
```
#### Program Input:
```
Enter 'e' for encryption and 'd' for decryption: d
Enter text to be decrypted:
3ad77bb40d7a3660a89ecaf32466ef97f5d3d58503b9699de785895a96fdbaaf43b1cd7f598ece23881b00e3ed0306887b0c785e27e8ad3f8223207104725dd4
Enter key: 2b7e151628aed2a6abf7158809cf4f3c
```
#### Output (Plaintext):
```
6bc1bee22e409f96e93d7e117393172aae2d8a571e03ac9c9eb76fac45af8e5130c81c46a35ce411e5fbc1191a0a52eff69f2445df4f9b17ad2b417be66c3710
```

3. 

