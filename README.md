# AES-in-ECB-Mode
Implementation of **AES encryption and decryption** in **Electronic Codebook (ECB)** mode using **C++**. <br>
Collaborators: Ralph Tan & Zukai Sagan

## Explanation of Design Decisions
In general we broke down the various functions/requirements listed the NIST doc into smaller functions to have more compartmentalized code logic. The AES program uses small helper functions like xtime() and mul() to handle the math behind AES encryption quickly. Padding and unpadding follow the PKCS#7 standard to ensure the data always fits into 16-byte blocks and that padding errors are safely handled. Each specific AES step like key expansion, subsitution, and mixing are separated into their own function for comprehensibility. With the main function and sprinkled throughout the program we included basic error handling as needed. Lastly, using the official NIST test vectors we show that the encryption and decryption results are accurate for various cases.

## To compile the program (for GNU C++ Compiler though similar for others):
```
g++ aes.cpp -o aes
```

## Run AES Program
```
./aes
```

## Respond to follow prompts accordingly





## Test Setup for Known AES-ECB Test Vectors

### 1. Open KAT_AES.zip
#### You should see a list of rsp files.

### 2. Open any rsp files, for example: ECBVarTxt128.rsp
#### You should see tests cases to encrypt (each test case has COUNT, KEY, PLAINTEXT, CIPHERTEXT)

### 3. Run the AES Program
#### To run the program:
```
./aes.exe
```
#### Enter 'e' for encryption
```
e
```
#### Enter the text to be encrypted, for example: Use Test Case COUNT=127
```
3f5b8cc9ea855a0afa7347d23e8d664e
```
#### Enter Key without any spaces/delimiters (Key for Test Case COUNT=127):
```
00000000000000000000000000000000
```
### 4. Resulting Text
#### The output should yield a corresponding output, plaintext, to the test case
#### Plaintext:
```
ffffffffffffffffffffffffffffffff
```

## Example Terminal Output:
```
.\aes.exe
Enter 'e' for encryption and 'd' for decryption: 
e
Enter text to be encrypted without spaces or delimiters: 
ffffffffffffffffffffffffffffffff
Enter key without spaces or delimiters: 
00000000000000000000000000000000
Resulting Text: 3f5b8cc9ea855a0afa7347d23e8d664e
```

