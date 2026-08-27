# HILL CIPHER
## NAME : SHALINI N
## REG NO : 212224040305
## EX. NO: 3 
## AIM:
 
IMPLEMENTATION OF HILL CIPHER
 
## To write a C program to implement the hill cipher substitution techniques.

## DESCRIPTION:

Each letter is represented by a number modulo 26. Often the simple scheme A = 0, B
= 1... Z = 25, is used, but this is not an essential feature of the cipher. To encrypt a message, each block of n letters is  multiplied by an invertible n × n matrix, against modulus 26. To
decrypt the message, each block is multiplied by the inverse of the m trix used for
 
encryption. The matrix used
 
for encryption is the cipher key, and it sho
 
ld be chosen
 
randomly from the set of invertible n × n matrices (modulo 26).


## ALGORITHM:

STEP-1: Read the plain text and key from the user. 

STEP-2: Split the plain text into groups of length three. 

STEP-3: Arrange the keyword in a 3*3 matrix.

STEP-4: Multiply the two matrices to obtain the cipher text of length three.

STEP-5: Combine all these groups to get the complete cipher text.

## PROGRAM 

```
#include <stdio.h>
#include <string.h>

int main() {
    int key[2][2], text[2], result[2];
    char plain[3], cipher[3];

    printf("Enter 2-letter plaintext (A-Z): ");
    scanf("%s", plain);

    printf("Enter the 2x2 key matrix:\n");

    for (int i = 0; i < 2; i++) {
        for (int j = 0; j < 2; j++) {
            scanf("%d", &key[i][j]);
        }
    }

    
    for (int i = 0; i < 2; i++) {
        text[i] = plain[i] - 'A';
    }

    
    for (int i = 0; i < 2; i++) {
        result[i] = 0;

        for (int j = 0; j < 2; j++) {
            result[i] += key[i][j] * text[j];
        }

        result[i] = result[i] % 26;
        cipher[i] = result[i] + 'A';
    }

    cipher[2] = '\0';

    printf("Cipher Text: %s\n", cipher);

    return 0;
}

```
## OUTPUT

<img width="1283" height="550" alt="image" src="https://github.com/user-attachments/assets/432f4b06-cfcf-4d3c-ba93-cf28abe37259" />

## RESULT

Thus the program was executed successfully.
