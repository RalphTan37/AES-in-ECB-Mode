# AES-in-ECB-Mode
Implementing AES encryption and decryption in Electronic Code Book (ECB) mode using C++

You can run a c++ file assuming you have "clank" with a comman g++ aes.cpp -o a (a being the name you want to use for the file) then running with ./a (no command line arguments).

Example tests (all are known test vectors with matching results): 

1. encryption, plaintext = 6bc1bee22e409f96e93d7e117393172aae2d8a571e03ac9c9eb76fac45af8e5130c81c46a35ce411e5fbc1191a0a52eff69f2445df4f9b17ad2b417be66c3710, key = 2b7e151628aed2a6abf7158809cf4f3c

Enter 'e' for encryption and 'd' for decryption: 
e
Enter text to be encrypted: 
6bc1bee22e409f96e93d7e117393172aae2d8a571e03ac9c9eb76fac45af8e5130c81c46a35ce411e5fbc1191a0a52eff69f2445df4f9b17ad2b417be66c3710
Enter key: 
2b7e151628aed2a6abf7158809cf4f3c
Resulting Text: 3ad77bb40d7a3660a89ecaf32466ef97f5d3d58503b9699de785895a96fdbaaf43b1cd7f598ece23881b00e3ed0306887b0c785e27e8ad3f8223207104725dd4

2. decryption, ciphertext = 3ad77bb40d7a3660a89ecaf32466ef97f5d3d58503b9699de785895a96fdbaaf43b1cd7f598ece23881b00e3ed0306887b0c785e27e8ad3f8223207104725dd4, key = 2b7e151628aed2a6abf7158809cf4f3c

Enter 'e' for encryption and 'd' for decryption: 
d
Enter text to be decrypted:
3ad77bb40d7a3660a89ecaf32466ef97f5d3d58503b9699de785895a96fdbaaf43b1cd7f598ece23881b00e3ed0306887b0c785e27e8ad3f8223207104725dd4
Enter key: 
2b7e151628aed2a6abf7158809cf4f3c
Resulting Text: 6bc1bee22e409f96e93d7e117393172aae2d8a571e03ac9c9eb76fac45af8e5130c81c46a35ce411e5fbc1191a0a52eff69f2445df4f9b17ad2b417be66c3710

3. 

