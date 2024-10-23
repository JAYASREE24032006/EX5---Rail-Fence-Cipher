# EX5 - RAIL FENCE CIPHER
## AIM :
To implement a program to encrypt a plain text and decrypt a cipher text using Rail Fence Cipher substitution technique.
## THEORM :
The Rail Fence Cipher is a type of transposition cipher where plaintext is written in a zigzag pattern across multiple rows (like rails of a fence) and then read row by row to form the ciphertext. It's a simple encryption technique used for obscuring messages.
## ALGORITHM :
### STEP 1 :
Design of Rail Fence Cipher algorithnm

### STEP 2 :
Implementation using C or pyhton code

### STEP 3 :
Testing algorithm with different key values.


## PROGRAM :
```
#include <stdio.h>
#include <string.h>
int main() 
{
    int i, j, k, l;
    char a[20], c[20], d[20];
    printf("\n\t\tRAIL FENCE TECHNIQUE");
    printf("\n\nEnter the input string : ");
    fgets(a, sizeof(a), stdin);
    a[strcspn(a, "\n")] = '\0'; 
    l = strlen(a):
    j = 0;
    for (i = 0; i < l; i++) 
    {
        if (i % 2 == 0)
        {
            c[j++] = a[i];
        }
    }
    for (i = 0; i < l; i++) 
    {
        if (i % 2 == 1) 
        {
            c[j++] = a[i];
        }
    }
    c[j] = '\0';
    printf("\nCipher text after applying rail fence : ");
    printf("%s", c);
    if (l % 2 == 0) 
    {
        k = l / 2;
    }
    else 
    {
        k = (l / 2) + 1;
    }
    j = 0;
    for (i = 0; i < k; i++) 
    {
        d[j] = c[i];
        j = j + 2;
    }
    j = 1;
    for (i = k; i < l; i++) 
    {
        d[j] = c[i];
        j = j + 2;
    }
    d[l] = '\0'; // Null-terminate the decrypted text
    printf("\nText after decryption : ");
    printf("%s", d);
    return 0;
}

```

 
## OUTPUT :
![image](https://github.com/user-attachments/assets/962d4b37-3ebe-4d77-a299-e2efce84f4f2)



## RESULT :
The program to encrypt a plain text and decrypt a cipher text using Rail Fence Cipher substitution technique is executed successfully.

