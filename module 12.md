Advanced-C-Lab-Manual
EXP NO 26: C PROGRAM TO DISPLAY STACK ELEMENTS USING LINKED LIST.
Aim:
To write a C program to display stack elements using linked list.

Algorithm:
Define a structure Node with two members: data to store the integer value and next to point to the next node in the linked list. Declare a global variable head representing the starting node of the linked list. Define a function display to print the elements of the linked list. Declare a pointer p and initialize it with the head of the linked list. Use a while loop to traverse the linked list: Print the data of the current node. Move to the next node using the next pointer.

Program:
#include <stdio.h>
#include <stdlib.h>
struct Node   
{  
int data;  
struct Node *next;  
}*head;  
void display()  
{  
    struct Node *temp;
    temp=head;
    while(temp!=NULL)
    {
        printf("%d\n",temp->data);
        temp=temp->next;
    }
}
void push(int data)  
{  
    struct Node *temp = (struct Node *)malloc(sizeof(struct Node));
    temp->data=data;
    temp->next=head;
    head=temp;
}
int main()
{
    push(10);
    push(20);
    push(30);
    display();
}
Output:
image
Result:
Thus, the program to display stack elements using linked list is verified successfully.

EXP.NO 27: C PROGRAM TO POP AN ELEMENT FROM THE GIVEN STACK USING LINKED LIST.
Aim:
To write a C program to pop an element from the given stack using liked list.

Algorithm:
Check for Empty Stack If head is equal to NULL, Print "Stack is empty." Else Proceed to the next step. Set head to point to the next node in the stack.

Program:
#include <stdio.h>
#include <stdlib.h>
struct Node   
{  
int data;  
struct Node *next;  
}*head;  
void display()  
{  
    struct Node *temp;
    temp=head;
    while(temp!=NULL)
    {
        printf("%d\n",temp->data);
        temp=temp->next;
    }
}
void push(int data)  
{  
    struct Node *temp = (struct Node *)malloc(sizeof(struct Node));
    temp->data=data;
    temp->next=head;
    head=temp;
}
void pop()  
{  
    struct Node *ptr;
    if(head==NULL)
    {
        printf("stack is empty\n");
    }
    else
    {
        ptr=head;
        head=head->next;
        free(ptr);
    }
    printf("After pop: ");
}  
int main()
{
    push(10);
    push(20);
    push(30);
    display();
    pop();
    display();
}
Output:
image
Result:
Thus, the program to pop an element from the given stack using liked list is verified successfully.

EXP NO:28 C PROGRAM TO DISPLAY QUEUE ELEMENTS USING LINKED LIST.
Aim:
To write a C program to display queue elements using linked list.

Algorithm:
Check if Queue is Empty Display Queue Elements Print the data of the current node pointed to by front Update front to point to the next node. End the display function.

Program:
#include <stdio.h>
#include <stdlib.h>
struct Node   
{  
int data;  
struct Node *next;  
}*front=NULL,*rear=NULL;  
void display()  
{  
    struct Node *temp;
    temp=front;
    while(temp!=NULL)
    {
        printf("%d\n",temp->data);
        temp=temp->next;
    }
}
void enqueue(int data)
{
    struct Node *ptr=(struct Node *)malloc(sizeof(struct Node));
    ptr->data=data;
    ptr->next=NULL;
    if(front==NULL && rear==NULL)
    {
        front=rear=ptr;
    }
    else
    {
        rear->next=ptr;
        rear=ptr;
    }
} 
int main()
{
    enqueue(10);
    enqueue(20);
    enqueue(30);
    display();
    
}
Output:
image
Result:
Thus, the program to display queue elements using linked list is verified successfully.

EXP NO:29 C PROGRAM TO INSERT ELEMENTS IN QUEUE USING LINKED LIST
Aim:
To write a C program to insert elements in queue using linked list

Algorithm:
Allocate Memory for New Node Set Data and Next Pointer Check if Queue is Empty Set both front and rear to point to the new node p. Set the next pointer of the current rear to point to the new node p. End of Enqueue Operation

Program:
#include <stdio.h>
#include <stdlib.h>
struct Node   
{  
int data;  
struct Node *next;  
}*front=NULL,*rear=NULL;  
void display()  
{  
    struct Node *temp;
    temp=front;
    while(temp!=NULL)
    {
        printf("%d\n",temp->data);
        temp=temp->next;
    }
}
void enqueue(int data)
{
    struct Node *ptr=(struct Node *)malloc(sizeof(struct Node));
    ptr->data=data;
    ptr->next=NULL;
    if(front==NULL && rear==NULL)
    {
        front=rear=ptr;
    }
    else
    {
        rear->next=ptr;
        rear=ptr;
    }
} 
int main()
{
    enqueue(10);
    enqueue(20);
    enqueue(30);
    display();
    
}
Output:
image
Result:
Thus, the program to insert elements in queue using linked list is verified successfully.

EXP NO:30 C FUNCTION TO FIND THE PEEK OF QUEUE USING LINKED LIST.
Aim:
The aim of this function is to retrieve the "peek" (the front element) of a queue implemented using a linked list

Algorithm:
Check if the queue is empty: o If the queue is empty (i.e., the front pointer is NULL), return an error or a message indicating that the queue is empty. Access the front element: o If the queue is not empty, return the data stored in the front node of the linked list (i.e., the element at the head of the queue).

Program:
#include <stdio.h>
#include <stdlib.h>
struct Node   
{  
int data;  
struct Node *next;  
}*front=NULL,*rear=NULL;  
void display()  
{  
    struct Node *temp;
    temp=front;
    while(temp!=NULL)
    {
        printf("%d\n",temp->data);
        temp=temp->next;
    }
}
void enqueue(int data)
{
    struct Node *ptr=(struct Node *)malloc(sizeof(struct Node));
    ptr->data=data;
    ptr->next=NULL;
    if(front==NULL && rear==NULL)
    {
        front=rear=ptr;
    }
    else
    {
        rear->next=ptr;
        rear=ptr;
    }
}
void peek()
{
    printf("peek:%d\n",front->data);
}
int main()
{
    enqueue(10);
    enqueue(20);
    enqueue(30);
    display();
    peek();
    
}
Output:
image
Result:
Thus, the program to retrieve the "peek" (the front element) of a queue implemented using a linked list is verified successfully.


