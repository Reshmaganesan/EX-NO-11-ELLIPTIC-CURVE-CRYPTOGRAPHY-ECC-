# EX-NO-11-ELLIPTIC-CURVE-CRYPTOGRAPHY-ECC

## Aim:
To Implement ELLIPTIC CURVE CRYPTOGRAPHY(ECC)


## ALGORITHM:

1. Elliptic Curve Cryptography (ECC) is a public-key cryptography technique based on the algebraic structure of elliptic curves over finite fields.

2. Initialization:
   - Select an elliptic curve equation \( y^2 = x^3 + ax + b \) with parameters \( a \) and \( b \), along with a large prime \( p \) (defining the finite field).
   - Choose a base point \( G \) on the curve, which will be used for generating public keys.

3. Key Generation:
   - Each party selects a private key \( d \) (a random integer).
   - Calculate the public key as \( Q = d \times G \) (using elliptic curve point multiplication).

4. Encryption and Decryption:
   - Encryption: The sender uses the recipient’s public key and the base point \( G \) to encode the message.
   - Decryption: The recipient uses their private key to decode the message and retrieve the original plaintext.

5. Security: ECC’s security relies on the Elliptic Curve Discrete Logarithm Problem (ECDLP), making it highly secure with shorter key lengths compared to traditional methods like RSA.

## Program:
```
#include <stdio.h>

int main()
{
    int d, Gx, Gy;
    int Qx, Qy;

    printf("Elliptic Curve Cryptography (ECC) Key Generation\n");

    // Input private key
    printf("Enter private key (d): ");
    scanf("%d", &d);

    // Input base point coordinates
    printf("Enter base point Gx: ");
    scanf("%d", &Gx);

    printf("Enter base point Gy: ");
    scanf("%d", &Gy);

    /* Public key generation (simplified multiplication) */
    Qx = d * Gx;
    Qy = d * Gy;

    // Output public key
    printf("\nPublic Key Q(x,y) = (%d , %d)\n", Qx, Qy);

    return 0;
}

```



## Output:


![fb2c9de8-995e-472f-b04c-9a6297dbc594](https://github.com/user-attachments/assets/b47e2765-b2b5-415d-b392-d7b4454aae49)


## Result:
The program is executed successfully

