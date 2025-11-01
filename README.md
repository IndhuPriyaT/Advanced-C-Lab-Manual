# Advanced-C-Lab-Manual
# EXP NO:11 C PROGRAM TO DISPLAY STACK ELEMENTS USING AN ARRAY.

## Aim: 

To write a C program to display stack elements using an array. 

## Algorithm:

Include Necessary Header Files
Declare Global Variables
Define the Display Function
Main Function (or Other Relevant Code)
Initialize the stack and top as needed.
Perform stack operations (push, pop, etc.).
Use the display function to visualize the stack's contents

## Program:

```
#include <stdio.h>
void push(int);
void display();
void pop();
#define SIZE 5
int stack[SIZE];
int TOP=-1;
int main()
{
  push (10);
  push(20);
  push(30);
  push(40);
  push(50);
  push(60);
  push(70);
  display();
  pop();
  display();
  push(70);
  display();
  
}
void push(int data)
{
  if (TOP==(SIZE-1))
    printf("\nStack Overflow !!! so can't push %d",data);
  else
  {
    TOP++;
    stack[TOP]=data;
    printf("\n  %d is pushed in to the stack",stack[TOP]);
  }
}

void display()
{
  if(TOP==-1)
    printf("Stack is Underflow!!");
  else
  {
    printf("\n Stack Contains: ");
    for(int i=TOP; i>=0; i--)
    {
      printf("-->%d",stack[i]);
      
    }
}
}

void pop()
{
  if(TOP==-1)
    printf("\n Stack is Underflow so cant do pop()");
  else
    {
      printf("\n The popped element is %d",stack[TOP]);
      TOP--;
    }
}
```

## Output:

<img width="487" height="407" alt="image" src="https://github.com/user-attachments/assets/c3b93e31-9de2-4dc6-a404-5ec2de884bde" />


## Result: 

Thus, the program to display stack elements using an array is verified successfully.

# EXP NO:12 PROGRAM TO PUSH THE GIVEN ELEMENT IN TO A STACK USING ARRAY. 

## Aim:

To create a C program to push the given element in to a stack using array. 

## Algorithm:

Declare global variables for the stack size, top index, and the stack itself.

Define the push function to add a floating-point number to the stack.

Initialize the stack size, top index, and the stack itself

Call the push function as needed.


## Program:

```
#include <stdio.h>
void push(int);
void display();
void pop();
#define SIZE 5
int stack[SIZE];
int TOP=-1;
int main()
{
  push (10);
  push(20);
  push(30);
  push(40);
  push(50);
  push(60);
  push(70);
  
}
void push(int data)
{
  if (TOP==(SIZE-1))
    printf("\nStack Overflow !!! so can't push %d",data);
  else
  {
    TOP++;
    stack[TOP]=data;
    printf("\n  %d is pushed in to the stack",stack[TOP]);
  }
}
```

## Output:

<img width="443" height="280" alt="image" src="https://github.com/user-attachments/assets/4c1a4624-908d-4b43-8ad2-c579465ea6d8" />


## Result:

Thus, the program to push the given element in to a stack using array is verified successfully.


# EXP NO:13 C PROGRAM TO DISPLAY QUEUE ELEMENTS USING ARRAY. 

## Aim: 

To write a C program to display queue elements using array

## Algorithm:

Declare global variables for the queue, rear, front, and iteration.

Define the display function to print the elements of the queue.

Initialize the queue, rear, and front as needed.

Call the display function and perform other queue operations as needed.


## Program:

```
#include <stdio.h>
#define MAX 5
int Queue[ MAX ];
int front =-1;
int rear =-1;
void enqueue(int);
void dequeue();
void display();
int main()
{
  display();
   enqueue(10);enqueue(20);enqueue(30);enqueue(40);
   display();
   dequeue();
   enqueue(70);
   display();
   
}

void enqueue(int element)
{
  if( rear == MAX-1)
    printf("\n Queue is overflow!! can't insert %d",element);
  else
  {
    if(front ==-1)
    {
      front =0;
    }
    rear++;
    Queue[rear]=element;
    printf("\n The %d is enqueued ",Queue[rear]);
  }
}


void dequeue()
{
  if( rear == -1 || front > rear)
  {
    printf( "\n Queue is UnderFloW!!");
  }
  else
  {
    printf( "\n The %d is dequeued from the queue",Queue[front]);
    front++;
    if(front > rear)
    {
    front =-1 ; rear =-1;
    }
  }
}

void display()
{
  if( rear == -1 || front > rear)
    printf("\n Queue is Underflow!!");
  else
  {
    printf("\n Queue has: ");
    for(int i= front; i<= rear; i++)
    {
      printf("--> %d",Queue[i]);
    }
  }
}
```


## Output:

<img width="448" height="325" alt="image" src="https://github.com/user-attachments/assets/e11a070a-591f-4654-a2a5-44a53d154946" />


## Result: 

Thus, the program to display queue elements using array is verified successfully.

# EXP NO:14 C PROGRAM TO INSERT ELEMENTS IN QUEUE USING ARRAY. 

## Aim:

To write a C program to insert elements in queue using array.

## Algorithm:

Declare global variables for the size, rear, front, and the queue itself.

Define the enqueue function to add a float to the queue.

Initialize the rear, front, and size of the queue as needed.

Call the enqueue function as needed.


## Program:

```
#include <stdio.h>
#define MAX 5
int Queue[ MAX ];
int front =-1;
int rear =-1;
void enqueue(int);
void dequeue();
void display();
int main()
{
   enqueue(10);enqueue(20);enqueue(30);enqueue(40);
   
}

void enqueue(int element)
{
  if( rear == MAX-1)
    printf("\n Queue is overflow!! can't insert %d",element);
  else
  {
    if(front ==-1)
    {
      front =0;
    }
    rear++;
    Queue[rear]=element;
    printf("\n The %d is enqueued ",Queue[rear]);
  }
}
```

## Output:

<img width="382" height="203" alt="image" src="https://github.com/user-attachments/assets/370c501d-0d29-4753-adc6-ed2eb87d2ef8" />


## Result:

Thus, the program to insert elements in queue using array is verified successfully.

# EXP NO:15 C FUNCTION TO DELETE ELEMENTS IN QUEUE USING ARRAY

## Aim:

To create a function in C that deletes an element from a queue implemented using an array.

## Algorithm:

Check if the Queue is Empty o If the front pointer is -1, it means the queue is empty, and there are no elements to delete. Print a message indicating that the queue is empty.
Delete the Front Element o If the queue is not empty, the element at the front index is deleted. o Increment the front pointer by 1 to remove the element and point to the next element in the queue.
Check if the Queue Becomes Empty After Deletion: o After deletion, check if the front pointer has passed the rear pointer (front > rear). If this is true, reset both front and rear to -1, indicating that the queue is now empty.
End the Function.

## Program:

```
#include <stdio.h>
#define MAX 5
int Queue[ MAX ];
int front =-1;
int rear =-1;
void enqueue(int);
void dequeue();
void display();
int main()
{
   enqueue(10);enqueue(20);enqueue(30);enqueue(40);
   dequeue();
   dequeue();
}

void enqueue(int element)
{
  if( rear == MAX-1)
    printf("\n Queue is overflow!! can't insert %d",element);
  else
  {
    if(front ==-1)
    {
      front =0;
    }
    rear++;
    Queue[rear]=element;
    printf("\n The %d is enqueued ",Queue[rear]);
  }
}


void dequeue()
{
  if( rear == -1 || front > rear)
  {
    printf( "\n Queue is UnderFloW!!");
  }
  else
  {
    printf( "\n The %d is dequeued from the queue",Queue[front]);
    front++;
    if(front > rear)
    {
    front =-1 ; rear =-1;
    }
  }
}



```

## Output:

<img width="407" height="248" alt="image" src="https://github.com/user-attachments/assets/fdc25566-049b-4489-a4ad-c2b6a623f2b7" />


## Result: 

Thus, the function that deletes an element from a queue implemented using an array is verified successfully.
