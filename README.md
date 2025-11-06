# AES-in-ECB-Mode
Implementation of **AES encryption and decryption** in **Electronic Codebook (ECB)** mode using **C++**. <br>
Collaborators: Ralph Tan & Zukai Sagan

## Explanation of Design Decisions
In general we broke down the various functions/requirements listed the NIST doc into smaller functions to have more compartmentalized code logic. The AES program uses small helper functions like xtime() and mul() to handle the math behind AES encryption quickly. Padding and unpadding follow the PKCS#7 standard to ensure the data always fits into 16-byte blocks and that padding errors are safely handled. Each specific AES step like key expansion, subsitution, and mixing are separated into their own function for comprehensibility. With the main function and sprinkled throughout the program we included basic error handling as needed. Lastly, using the official NIST test vectors we made sure that the encryption and decryption results are accurate for various edge cases.

## To compile the program (for GNU C++ Compiler though similar for others):
```
g++ aes.cpp -o aes
```

## Run AES Program
```
./aes
```

## Respond to follow prompts accordingly





## Examples

### 1. 
#### Enter 'e' for encryption
```
e
```
#### Enter the text to be encrypted without spaces/delimiters
```
ffffffffffffffffffffffffffffffff
```
#### Enter key without spaces/delimiters
```
00000000000000000000000000000000
```
### Resulting text
```
3f5b8cc9ea855a0afa7347d23e8d664e
```

## Example Terminal Output:
```
./aes
Enter 'e' for encryption and 'd' for decryption: 
e
Enter text to be encrypted without spaces or delimiters: 
ffffffffffffffffffffffffffffffff
Enter key without spaces or delimiters: 
00000000000000000000000000000000
Resulting Text: 3f5b8cc9ea855a0afa7347d23e8d664e
```

### 2.
#### Enter 'd' for decryption
```
d
```
#### Enter the text to be decrypted without spaces/delimiters
```
3f5b8cc9ea855a0afa7347d23e8d664e
```
#### Enter key without spaces/delimiters
```
00000000000000000000000000000000
```
### Resulting text
```
ffffffffffffffffffffffffffffffff
```

## Example Terminal Output:
```
./aes
Enter 'e' for encryption and 'd' for decryption: 
d
Enter text to be decrypted without spaces or delimiters: 
3f5b8cc9ea855a0afa7347d23e8d664e
Enter key without spaces or delimiters: 
00000000000000000000000000000000
Resulting Text: ffffffffffffffffffffffffffffffff
```

### 3.
#### Enter 'e' for encryption
```
e
```
#### Enter the text to be encrypted without spaces/delimiters
```
6bc1bee22e409f96e93d7e117393172aae2d8a571e03ac9c9eb76fac45af8e5130c81c46a35ce411e5fbc1191a0a52eff69f2445df4f9b17ad2b417be66c3710
```
#### Enter key without spaces/delimiters
```
2b7e151628aed2a6abf7158809cf4f3c
```
### Resulting text
```
3ad77bb40d7a3660a89ecaf32466ef97f5d3d58503b9699de785895a96fdbaaf43b1cd7f598ece23881b00e3ed0306887b0c785e27e8ad3f8223207104725dd4
```

## Example Terminal Output:
```
./aes
Enter 'e' for encryption and 'd' for decryption: 
e
Enter text to be encrypted without spaces or delimiters: 
6bc1bee22e409f96e93d7e117393172aae2d8a571e03ac9c9eb76fac45af8e5130c81c46a35ce411e5fbc1191a0a52eff69f2445df4f9b17ad2b417be66c3710
Enter key without spaces or delimiters: 
2b7e151628aed2a6abf7158809cf4f3c
Resulting Text: 3ad77bb40d7a3660a89ecaf32466ef97f5d3d58503b9699de785895a96fdbaaf43b1cd7f598ece23881b00e3ed0306887b0c785e27e8ad3f8223207104725dd4
```


### 4.
#### Enter 'd' for decryption
```
d
```
#### Enter the text to be decrypted without spaces/delimiters
```
3ad77bb40d7a3660a89ecaf32466ef97f5d3d58503b9699de785895a96fdbaaf43b1cd7f598ece23881b00e3ed0306887b0c785e27e8ad3f8223207104725dd4
```
#### Enter key without spaces/delimiters
```
2b7e151628aed2a6abf7158809cf4f3c
```
### Resulting text
```
6bc1bee22e409f96e93d7e117393172aae2d8a571e03ac9c9eb76fac45af8e5130c81c46a35ce411e5fbc1191a0a52eff69f2445df4f9b17ad2b417be66c3710
```

## Example Terminal Output:
```
./aes
Enter 'e' for encryption and 'd' for decryption: 
d
Enter text to be decrypted without spaces or delimiters: 
3ad77bb40d7a3660a89ecaf32466ef97f5d3d58503b9699de785895a96fdbaaf43b1cd7f598ece23881b00e3ed0306887b0c785e27e8ad3f8223207104725dd4
Enter key without spaces or delimiters: 
2b7e151628aed2a6abf7158809cf4f3c
Resulting Text: 6bc1bee22e409f96e93d7e117393172aae2d8a571e03ac9c9eb76fac45af8e5130c81c46a35ce411e5fbc1191a0a52eff69f2445df4f9b17ad2b417be66c3710
```


### 5.
#### Enter 'e' for encryption
```
e
```
#### Enter the text to be encrypted without spaces/delimiters
```
e5b2d8f1a7c3e9b0d6f4a1c8e2b7d5f9a3c0e6b1d4f8a9c2e7b5d0f3a6c1e9b4d8f2a5c7e0b3d6f1a9c4e8b2d5f7a0c3e6b9d1f4a8c2e5b7d0f3a6c9e1b4d8f2a5c7e0
```
#### Enter key without spaces/delimiters
```
a3f7b9e2c1d4f68a0b5e7c9d1f3a6b8e
```
### Resulting text
```
7574dcb540052fce39a390b7c1a1f63a864ae2e85bce7fbb1aef081efc31a1342158e08a245aa4e1851f4a171f6c0c709781e8c5959a6ae08ff76335c731a751e3c3dab2da8ad69c2e660cb562354271
```

## Example Terminal Output:
```
./aes
Enter 'e' for encryption and 'd' for decryption: 
e
Enter text to be encrypted without spaces or delimiters: 
e5b2d8f1a7c3e9b0d6f4a1c8e2b7d5f9a3c0e6b1d4f8a9c2e7b5d0f3a6c1e9b4d8f2a5c7e0b3d6f1a9c4e8b2d5f7a0c3e6b9d1f4a8c2e5b7d0f3a6c9e1b4d8f2a5c7e0
Enter key without spaces or delimiters: 
a3f7b9e2c1d4f68a0b5e7c9d1f3a6b8e
Resulting Text: 7574dcb540052fce39a390b7c1a1f63a864ae2e85bce7fbb1aef081efc31a1342158e08a245aa4e1851f4a171f6c0c709781e8c5959a6ae08ff76335c731a751e3c3dab2da8ad69c2e660cb562354271
```

### 6.
#### Enter 'd' for decryption
```
d
```
#### Enter the text to be decrypted without spaces/delimiters
```
7574dcb540052fce39a390b7c1a1f63a864ae2e85bce7fbb1aef081efc31a1342158e08a245aa4e1851f4a171f6c0c709781e8c5959a6ae08ff76335c731a751e3c3dab2da8ad69c2e660cb562354271
```
#### Enter key without spaces/delimiters
```
a3f7b9e2c1d4f68a0b5e7c9d1f3a6b8e
```
### Resulting text
```
e5b2d8f1a7c3e9b0d6f4a1c8e2b7d5f9a3c0e6b1d4f8a9c2e7b5d0f3a6c1e9b4d8f2a5c7e0b3d6f1a9c4e8b2d5f7a0c3e6b9d1f4a8c2e5b7d0f3a6c9e1b4d8f2a5c7e0
```

## Example Terminal Output:
```
./aes
Enter 'e' for encryption and 'd' for decryption: 
d
Enter text to be decrypted without spaces or delimiters: 
7574dcb540052fce39a390b7c1a1f63a864ae2e85bce7fbb1aef081efc31a1342158e08a245aa4e1851f4a171f6c0c709781e8c5959a6ae08ff76335c731a751e3c3dab2da8ad69c2e660cb562354271
Enter key without spaces or delimiters: 
a3f7b9e2c1d4f68a0b5e7c9d1f3a6b8e
Resulting Text: e5b2d8f1a7c3e9b0d6f4a1c8e2b7d5f9a3c0e6b1d4f8a9c2e7b5d0f3a6c1e9b4d8f2a5c7e0b3d6f1a9c4e8b2d5f7a0c3e6b9d1f4a8c2e5b7d0f3a6c9e1b4d8f2a5c7e0
```


