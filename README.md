# EX5 - RAIL FENCE CIPHER
## AIM :
To implement a program to encrypt a plain text and decrypt a cipher text using Rail Fence Cipher substitution technique.

## DESIGN STEPS :
### STEP 1 :
Design of Rail Fence Cipher algorithnm

### STEP 2 :
Implementation using C or pyhton code

### STEP 3 :
Testing algorithm with different key values.

## ALGORITHM DESCRIPTION :
In the rail fence cipher, the plaintext is written downwards and diagonally on successive "rails" of an imaginary fence, then moving up when we reach the bottom rail. When we reach the top rail, the message is written downwards again until the whole plaintext is written out. The message is then read off in rows.

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

