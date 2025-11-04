# Advanced-C-Lab-Manual
# Advanced-C-Lab-Manual
# EXP NO:21 C PROGRAM TO CREATE A FUNCTION TO FIND THE GREATEST NUMBER 

## Aim: 

To write a C program to create a function to find the greatest number

## Algorithm:

Include the necessary header #include <stdio.h>.
Use a series of if and else if statements to compare the values and return the maximum among them.
Declare variables n1, n2, n3, n4, and greater to store user input and the result.
Use scanf to take four integers as input.
Call the max_of_four function with the input integers and store the result in the greater variable

## Program: 

```
#include <stdio.h>

int max_of_four(int n1, int n2, int n3, int n4) {
    if (n1 >= n2 && n1 >= n3 && n1 >= n4)
        return n1;
    else if (n2 >= n1 && n2 >= n3 && n2 >= n4)
        return n2;
    else if (n3 >= n1 && n3 >= n2 && n3 >= n4)
        return n3;
    else
        return n4;
}

int main() {
    int n1, n2, n3, n4, greater;
    scanf("%d %d %d %d", &n1, &n2, &n3, &n4);
    greater = max_of_four(n1, n2, n3, n4);
    printf("%d", greater);
    return 0;
}

```

## Output: 

<img width="494" height="160" alt="image" src="https://github.com/user-attachments/assets/29c474a8-7ed0-45d0-9580-d1fa30f9a457" />


## Result: 

Thus, the program that create a function to find the greatest number is verified successfully.

# EXP NO:22 C PROGRAM TO PRINT THE MAXIMUM VALUES FOR THE AND, OR AND XOR COMPARISONS 

## Aim: 

To write a C program to print the maximum values for the AND, OR and XOR comparisons

## Algorithm:

Define a function calculate_the_max that takes two integers n and k as parameters.
Declare variables a, o, and x to store the maximum values for AND, OR, and XOR operations, respectively.
Use nested loops to iterate through pairs of integers (i, j) from 1 to n.
Within the loops, check conditions for AND, OR, and XOR operations and update the corresponding maximum values (a, o, x).
Declare variables n and k to store user input.
Use scanf to take two integers as input.
Call the calculate_the_max function with input values.

## Program: 

```
#include <stdio.h>

void calculate_the_max(int n, int k) {
    int a = 0, o = 0, x = 0;
    for (int i = 1; i <= n; i++) {
        for (int j = i + 1; j <= n; j++) {
            int and_val = i & j;
            int or_val = i | j;
            int xor_val = i ^ j;

            if (and_val < k && and_val > a)
                a = and_val;
            if (or_val < k && or_val > o)
                o = or_val;
            if (xor_val < k && xor_val > x)
                x = xor_val;
        }
    }
    printf("%d\n%d\n%d\n", a, o, x);
}

int main() {
    int n, k;
    scanf("%d %d", &n, &k);
    calculate_the_max(n, k);
    return 0;
}

```

## Output: 

<img width="440" height="191" alt="image" src="https://github.com/user-attachments/assets/697033eb-31a7-414f-935b-243811fff474" />


## Result: 

Thus, the program to print the maximum values for the AND, OR and XOR comparisons is verified successfully.

# EXP NO:23 C PROGRAM TO WRITE THE LOGIC FOR THE REQUESTS

## Aim: 

To write a C program to write the logic for the requests

## Algorithm:

Declare variables noshel and noque to store the number of shelves and the number of queries, respectively.
Use scanf to take two integers as input for the number of shelves and queries.
Declare a 2D array shelarr to represent shelves and books, and an array nobookarr to store the number of books on each shelf.
Declare variables k and c to keep track of the book index and the total number of books.
Use a for loop to iterate over the queries.

## Program: 

```
#include <stdio.h>
#include <stdlib.h>

int main() {
    int noshel, noque;
    scanf("%d", &noshel);
    scanf("%d", &noque);

    int *nobookarr = (int *)calloc(noshel, sizeof(int));
    int **shelarr = (int **)malloc(noshel * sizeof(int *));
    for (int i = 0; i < noshel; i++) {
        shelarr[i] = NULL;
    }

    for (int i = 0; i < noque; i++) {
        int type;
        scanf("%d", &type);

        if (type == 1) {
            int x, y;
            scanf("%d %d", &x, &y);
            nobookarr[x]++;
            shelarr[x] = realloc(shelarr[x], nobookarr[x] * sizeof(int));
            shelarr[x][nobookarr[x] - 1] = y;
        } 
        else if (type == 2) {
            int x, y;
            scanf("%d %d", &x, &y);
            printf("%d\n", shelarr[x][y]);
        } 
        else if (type == 3) {
            int x;
            scanf("%d", &x);
            printf("%d\n", nobookarr[x]);
        }
    }

    for (int i = 0; i < noshel; i++) {
        free(shelarr[i]);
    }
    free(shelarr);
    free(nobookarr);

    return 0;
}


```

## Output: 

<img width="491" height="322" alt="image" src="https://github.com/user-attachments/assets/0368d803-1d61-4478-b18c-691bb5970f47" />


## Result: 

Thus, the program to write the logic for the requests is verified successfully.

# EXP NO:24 C PROGRAM PRINT THE SUM OF THE INTEGERS IN THE ARRAY. 

## Aim: 

To write a C program print the sum of the integers in the array.

## Algorithm:

Declare a variable n to store the number of integers.
Use scanf to take an integer n as input.
Declare an array a of size n to store the integers.
Declare a variable sum and initialize it to zero.
Use a for loop to iterate n times:
Use scanf to input each integer and add it to the sum.
Print the final sum using printf.

## Program: 

```
#include <stdio.h>
int main()
{
    int n,i,s=0,arr[100];
    scanf("%d",&n);
    for(i=0;i<n;i++)
    {
        scanf("%d",&arr[i]);
    }
    for(i=0;i<n;i++)
    {
        s+=arr[i];
    }
    printf("%d",s);
}

```

## Output:

<img width="429" height="138" alt="image" src="https://github.com/user-attachments/assets/b9eae9f3-6121-458d-a520-f54bffd7b14f" />


## Result: 

Thus, the program prints the sum of the integers in the array is verified successfully.

# EXP NO 25: C PROGRAM TO COUNT THE NUMBER OF WORDS IN A SENTENCE

## Aim:

To write a C program that counts the number of words in a given sentence.

## Algorithm:

Input the sentence: Take a sentence from the user.
Initialize a counter variable: This will keep track of the number of words.
Process each character of the sentence: o Iterate through the sentence, checking each character. o If a character is not a space, it may belong to a word. If it's the first non-space character after a space or at the start, increment the word count.
Handle spaces and punctuation: Skip over spaces, punctuation marks, and consider each word as a sequence of characters separated by spaces.
Display the result: After processing the sentence, output the total word count.

## Program: 

```
#include <stdio.h>
#include <ctype.h>

int main() {
    char sentence[200];
    int count = 0, inWord = 0;

    printf("Enter a sentence: ");
    fgets(sentence, sizeof(sentence), stdin);

    for (int i = 0; sentence[i] != '\0'; i++) {
        if (!isspace(sentence[i]) && ispunct(sentence[i]) == 0) {
            if (inWord == 0) {
                count++;
                inWord = 1;
            }
        } else {
            inWord = 0;
        }
    }

    printf("Total number of words: %d\n", count);
    return 0;
}
```

## Output: 

<img width="454" height="146" alt="image" src="https://github.com/user-attachments/assets/627221d1-ee14-43bc-9bd5-1323d680f698" />


## Result:

Thus, the program that counts the number of words in a given sentence is verified successfully.
