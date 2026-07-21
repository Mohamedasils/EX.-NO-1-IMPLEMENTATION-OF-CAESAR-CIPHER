# EX. NO: 1(A) : IMPLEMENTATION OF CAESAR CIPHER

## AIM:
To implement the simple substitution technique named Caesar cipher using C language.

## ALOGORITHM:

STEP-1: Read the plain text from the user.

STEP-2: Read the key value from the user.

STEP-3: If the key is positive then encrypt the text by adding the key with each character in the plain text.

STEP-4: Else subtract the key from the plain text.

STEP-5: Display the cipher text obtained above.

## PROGRAM:
```
#include <stdio.h>
#include <string.h>

void main()
{
    char text[100];
    int key, i, len;

    printf("Enter the plaintext: ");
    scanf("%s", text);

    printf("Enter the key: ");
    scanf("%d", &key);

    len = strlen(text);
    printf("\nEncrypted Text: ");
    for(i = 0; i < len; i++)
    {
        if(text[i] >= 'A' && text[i] <= 'Z')
            text[i] = ((text[i] - 'A' + key) % 26) + 'A';
        else if(text[i] >= 'a' && text[i] <= 'z')
            text[i] = ((text[i] - 'a' + key) % 26) + 'a';

        printf("%c", text[i]);
    }
    printf("\nDecrypted Text: ");
    for(i = 0; i < len; i++)
    {
        if(text[i] >= 'A' && text[i] <= 'Z')
            text[i] = ((text[i] - 'A' - key + 26) % 26) + 'A';
        else if(text[i] >= 'a' && text[i] <= 'z')
            text[i] = ((text[i] - 'a' - key + 26) % 26) + 'a';

        printf("%c", text[i]);
    }
}
```
## OUTPUT:

<img width="959" height="369" alt="Screenshot 2026-07-21 113907" src="https://github.com/user-attachments/assets/7c065403-d3cf-40c1-aa9e-dfea59c04562" />


## RESULT :
 Thus the implementation of ceasar cipher had been executed successfully.
