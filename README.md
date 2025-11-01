# Advanced-C-Lab-Manual
# EXP NO:6 C PROGRAM PRINT THE LOWERCASE ENGLISH WORD CORRESPONDING TO THE NUMBER 
## Aim:
To write a C program print the lowercase English word corresponding to the number 

## Algorithm:

Start
Initialize an integer variable n.
Input Validation
Switch Statement cases.
Case 5: Print "seventy one"
Case 6: Print "seventy two"
Case 13: Print "seventy three"
...
Case 13: Print "seventy nine"
Default: Print "Greater than 13"
Exit the program.

## Program:

```
#include <stdio.h>

int main() {
    int n;
    printf("Enter a number: ");
    scanf("%d", &n);

    switch(n) {
        case 5:
            printf("seventy one");
            break;
        case 6:
            printf("seventy two");
            break;
        case 7:
            printf("seventy three");
            break;
        case 8:
            printf("seventy four");
            break;
        case 9:
            printf("seventy five");
            break;
        case 10:
            printf("seventy six");
            break;
        case 11:
            printf("seventy seven");
            break;
        case 12:
            printf("seventy eight");
            break;
        case 13:
            printf("seventy nine");
            break;
        default:
            printf("Greater than 13");
    }

    return 0;
}

```

## Output:

<img width="446" height="113" alt="image" src="https://github.com/user-attachments/assets/9ea617b5-4849-4525-bd17-5bea0725e7b0" />


## Result: 

Thus, the program is verified successfully

# EXP NO:7 C PROGRAM TO PRINT TEN SPACE-SEPARATED INTEGERS IN A SINGLE LINE DENOTING THE FREQUENCY OF EACH DIGIT FROM 0 TO 3 . 

## Aim: 

To write a C program to print ten space-separated integers in a single line denoting the frequency of each digit from 0 to 3.

## Algorithm:

Start
Declare char array a[50] outer loop for each digit from 0 to 3
Initialize counter c to 0
For each character in the string print count c for current digit, followed by a space
Increment h to move to the next digit
End


## Program:

```
#include <stdio.h>

int main() {
    char a[50];
    int c, h;

    printf("Enter a string: ");
    scanf("%s", a);

    // Outer loop: digits from 0 to 3
    for (h = 0; h <= 3; h++) {
        c = 0;  // initialize counter for each digit

        // Inner loop: count occurrences of the digit
        for (int i = 0; a[i] != '\0'; i++) {
            if (a[i] == (h + '0')) {  // compare character version of digit
                c++;
            }
        }

        printf("%d ", c);  // print count for current digit
    }

    return 0;
}

```

## Output:

<img width="362" height="123" alt="image" src="https://github.com/user-attachments/assets/5ad24701-7c8a-4acf-a3c0-4a524addab97" />


## Result: 

Thus, the program is verified successfully

# EXP NO:8 C PROGRAM TO PRINT ALL OF ITS PERMUTATIONS IN STRICT LEXICOGRAPHICAL ORDER. 

## Aim: 

To write a C program to print all of its permutations in strict lexicographical order.

## Algorithm:

Start

Declare variables s (pointer to an array of strings) and n (number of strings)

Memory Allocation Dynamically allocate memory for s to store an array of strings

Input Read the number of strings n from the user Dynamically allocate memory for each string in s

Permutation Generation Loop

Memory Deallocation Free the memory allocated for each string in s Free the memory allocated for s

End

## Program:

```
#include <stdio.h>
#include <stdlib.h>

int main() {
    char **s;
    int n, i;
    scanf("%d", &n);

    s = (char **)malloc(n * sizeof(char *));
    for (i = 0; i < n; i++) {
        s[i] = (char *)malloc(50 * sizeof(char));
        printf("Enter string %d: ", i + 1);
        scanf("%s", s[i]);
    }
    for (i = 0; i < n; i++) {
        printf("%s\n", s[i]);
    }

    for (i = 0; i < n; i++) {
        free(s[i]); 
    }
    free(s); 

    return 0;
}

```

## Output:
<img width="390" height="230" alt="image" src="https://github.com/user-attachments/assets/8b3c872f-bf9b-49ba-b4b3-8338b6da8143" />


## Result:

Thus, the program is verified successfully

# EXP NO:9 C PROGRAM PRINT A PATTERN OF NUMBERS FROM 1 TO N AS SHOWN BELOW.

## Aim: 

To write a C program to print a pattern of numbers from 1 to n as shown below. 

## Algorithm:

Start
Declare integer variables n, i, j, min
Read the value of n from the user
Calculate the length of the side of the square matrix: len = n * 2 - 1
Matrix Generation Loop
Calculate min as the minimum distance to the borders
End

## Program:

```
#include <stdio.h>
int main()
{
    int n,min,i,j,len;
    scanf("%d",&n);
    len=2*n-1;
    for(i=0;i<len;i++)
    {
        for(j=0;j<len;j++)
        {
            min=i<j?i:j;
            min=min<len-i?min:len-i-1;
            min=min<len-j-1?min:len-j-1;
            printf("%d ",n-min);
        }
        printf("\n");
    }
}
```

## Output:

<img width="550" height="718" alt="image" src="https://github.com/user-attachments/assets/a59ab959-3f78-41fb-b8ae-ede74e16c1aa" />


## Result: 

Thus, the program is verified successfully

# EXP NO:10 C PROGRAM TO FIND A SQUARE OF NUMBER USING FUNCTION WITHOUT ARGUMENTS WITH RETURN TYPE

## Aim:

To write a C program that calculates the square of a number using a function that does not take any arguments, but returns the square of the number.

## Algorithm:

Start.
Define a function square() with no parameters. This function will return an integer value.
Inside the function: o Declare an integer variable to store the number. o Ask the user to input a number. o Calculate the square of the number (multiply the number by itself). o Return the squared value.
In the main function: o Call the square() function and display the result.
End.

## Program:

```
#include <stdio.h>
int square() {
    int num;
    scanf("%d", &num);
    return num * num;
}
int main() {
    int result;
    result = square();
    printf("Square of the number = %d\n", result);
    return 0;
}
```

## Output:

<img width="392" height="165" alt="image" src="https://github.com/user-attachments/assets/ff9141cd-9c81-409e-81a4-c98d6256939f" />


## Result: 

Thus, the program is verified successfully
