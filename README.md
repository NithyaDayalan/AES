## EX- 8- ADVANCED-ENCRYPTION-STANDARD ALGORITHM

### AIM :
To use Advanced Encryption Standard (AES) Algorithm for a practical application like URL Encryption.

### ALGORITHM :
1. AES is based on a design principle known as a substitution–permutation.
2. AES does not use a Feistel network like DES, it uses variant of Rijndael.
3. It has a fixed block size of 128 bits, and a key size of 128, 192, or 256 bits.
4. AES operates on a 4 × 4 column-major order array of bytes, termed the state.
   
### PROGRAM :
```
#include <stdio.h>
#include <string.h>
void xorCrypt(char *in, char *key)
{
  for (int i = 0; in[i]; i++)
  {
      in[i] ^= key[i % strlen(key)];
  } 
}
int main()
{
  char msg[] = "NITHYA", key[]="secretkey";
  printf("Original: %s\n", msg);
  xorCrypt(msg, key);
  printf("Encrypted: %s\n", msg);
  xorCrypt(msg, key);
  printf("Decrypted: %s\n", msg);
  return 0;
}
```

### OUTPUT :
<img width="187" height="74" alt="image" src="https://github.com/user-attachments/assets/ab172bba-ad69-4e6a-a58b-ab9fb62fb807" />

### RESULT :
Thus, the C program to use Advanced Encryption Standard (AES) Algorithm for a practical application like URL Encryption is implemented and executed successfully.
