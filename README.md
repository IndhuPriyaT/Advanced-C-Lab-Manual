# Advanced-C-Lab-Manual
# EXP NO:16 C PROGRAM TO SEARCH A GIVEN ELEMENT IN THE GIVEN LINKED LIST. 

## Aim: 

To write a C program to search a given element in the given linked list.

## Algorithm:

Define the structure for a node in a linked list.
Define the search function to find a specific character in the linked list.
Initialize the head of the linked list as needed.
Call the search function and perform other linked list operations as needed.

## Program:

```
#include <stdio.h>
#include <stdlib.h>

struct Node {
    char data;
    struct Node* next;
};

int main() {
    struct Node *head = NULL, *second = NULL, *third = NULL;
    char key;

    head = (struct Node*)malloc(sizeof(struct Node));
    second = (struct Node*)malloc(sizeof(struct Node));
    third = (struct Node*)malloc(sizeof(struct Node));

    head->data = 'A';
    head->next = second;

    second->data = 'B';
    second->next = third;

    third->data = 'C';
    third->next = NULL;

    printf("Linked list: A -> B -> C -> NULL\n");
    printf("Enter a character to search: ");
    scanf(" %c", &key);

    struct Node* temp = head;
    int found = 0, pos = 1;

    while (temp != NULL) {
        if (temp->data == key) {
            printf("Character '%c' found at position %d.\n", key, pos);
            found = 1;
            break;
        }
        temp = temp->next;
        pos++;
    }

    if (!found)
        printf("Character '%c' not found in the list.\n", key);

    return 0;
}

```

## Output:

<img width="464" height="203" alt="image" src="https://github.com/user-attachments/assets/3375500d-ec26-4d71-b9fc-f27062951c0d" />


## Result: 

Thus, the program to search a given element in the given linked list is verified successfully.

# EXP NO:17 PROGRAM TO INSERT A NODE IN A LINKED LIST.

## Aim:

To write a C program to insert a node in a linked list. 

## Algorithm:

Define the structure for a node in a linked list
Define the insert function to insert a new node with character data at the end of the linked list.
Initialize the head of the linked list as needed.
Call the insert function and perform other linked list operations as needed.

## Program:

```
#include<stdio.h>
# include <stdlib.h>
struct node 
{
    int data;
    struct node* next;
};


void printList(struct node* head) 
{
    struct node* temp = head;
    printf("\nSLL: ");
    while (temp != NULL) 
    {
        printf("%d -> ", temp->data);  
        temp = temp->next;            
    }
    printf("NULL\n");                 
}

void addFirst(struct node** head, int val)
{
    struct node* newNode = (struct node*)malloc(sizeof(struct node)); 
    newNode->data = val;  
    newNode->next = *head;    
    *head = newNode;          
}
int main() 
{
    struct node *head = NULL;  
    addFirst(&head,10);
    addFirst(&head,20);
    addFirst(&head,30);
    
    printList(head);
   
    

    return 0;
}

```

## Output:

<img width="435" height="183" alt="image" src="https://github.com/user-attachments/assets/6d8044b5-3e39-4729-88ab-086fe38e683c" />


## Result: 

Thus, the program to insert a node in a linked list is verified successfully.

# EXP NO:18 C PROGRAM TO TRAVERSE A DOUBLY LINKED LIST 

## Aim: 

To write a C program to traverse a doubly linked list.

## Algorithm:

Initialize a temporary pointer (temp) to the head of the list.
Use a while loop to traverse the list until the end (temp == NULL) is reached.
Inside the loop, print the data of the current node.
Move to the next node by updating the temp pointer to point to the next node (temp = temp->next).

## Program:

```
#include<stdio.h>
# include <stdlib.h>
struct Node
{
    struct Node *prev;
    struct Node *next;
    int data;
}*head;
void insert(int data)
{
    struct Node *ptr,*temp;
   ptr=(struct Node *)malloc(sizeof(struct Node));
   if(ptr==NULL)
   {       printf("OVERFLOW\n");
   }
   else
   {   ptr->data=data;
       if(head==NULL)
       {
           ptr->next=NULL;
           ptr->prev=NULL;
           head=ptr;
       }
       else
       {
          temp=head;
          while(temp->next!=NULL)
          {
              temp=temp->next;
          }
          temp->next=ptr;
          ptr->prev=temp;
          ptr->next=NULL;
        }
    }
}
void display()
{
    struct Node *temp=head;
    while(temp!=NULL)
    {
        printf("%d ",temp->data);
        temp=temp->next;
    }
}
int main() 
{
    struct node *head = NULL;  
    insert(10);
    insert(20);
    insert(30);
    display();
   
    

    return 0;
}

```

## Output:

<img width="536" height="133" alt="image" src="https://github.com/user-attachments/assets/46d251bd-db27-4e10-9086-5b465128b409" />


## Result: 

Thus, the program to traverse a doubly linked list is verified successfully.

# EXP NO:19 C PROGRAM TO INSERT AN ELEMENT IN DOUBLY LINKED LIST 

## Aim: 

To write a C program to insert an element in doubly linked list

## Algorithm:

Create a new node (newNode) and allocate memory for it.
Set the data of the new node to the provided value.
If the list is empty, set the new node as the head.
If the list is not empty, traverse the list to find the last node.
Set the new node's prev pointer to the last node and update the last node's next pointer to the new node.

## Program:

```
#include<stdio.h>
# include <stdlib.h>
struct Node
{
    struct Node *prev;
    struct Node *next;
    int data;
}*head;
void insert(int data)
{
    struct Node *ptr,*temp;
   ptr=(struct Node *)malloc(sizeof(struct Node));
   if(ptr==NULL)
   {       printf("OVERFLOW\n");
   }
   else
   {   ptr->data=data;
       if(head==NULL)
       {
           ptr->next=NULL;
           ptr->prev=NULL;
           head=ptr;
       }
       else
       {
          temp=head;
          while(temp->next!=NULL)
          {
              temp=temp->next;
          }
          temp->next=ptr;
          ptr->prev=temp;
          ptr->next=NULL;
        }
    }
}
void display()
{
    struct Node *temp=head;
    while(temp!=NULL)
    {
        printf("%d ",temp->data);
        temp=temp->next;
    }
}
int main() 
{
    struct node *head = NULL;  
    insert(10);
    insert(20);
    insert(30);
    display();
   
    

    return 0;
}


```

## Output:

<img width="354" height="90" alt="image" src="https://github.com/user-attachments/assets/29eecd9a-57c8-428f-813f-68bd7962ffee" />

## Result: 

Thus, the program to insert an element in doubly linked list is verified successfully.

# EXP NO:20 C FUNCTION TO DELETE A GIVEN ELEMENT IN THE GIVEN LINKED LIST

## Aim: 

To write a C function that deletes a given element from a linked list.

## Algorithm:

Check if the Linked List is Empty: o If the head of the linked list is NULL, print a message indicating the list is empty and exit the function.
Traverse the Linked List: o Start from the head node and iterate through the list to find the node that contains the given element (data).
Handle Deletion of the First Node: o If the element to be deleted is found in the head node:  Update the head of the linked list to point to the next node (i.e., head = head->next).  Free the memory allocated to the node to be deleted.  Exit the function.
Traverse and Delete from the Middle or End: o If the element is not in the head node, continue traversing the list by checking each node’s next pointer. o When the node with the element is found, update the previous node’s next pointer to point to the next node of the node to be deleted (prev->next = current->next). o Free the memory allocated to the node to be deleted.
Handle the Case when the Element is Not Found: o If the element is not found in any node, print a message indicating the element is not present in the list.
End the Function.

## Program:

```
#include<stdio.h>
# include <stdlib.h>
struct Node
{
    struct Node *prev;
    struct Node *next;
    int data;
}*head;
void insert(int data)
{
    struct Node *ptr,*temp;
   ptr=(struct Node *)malloc(sizeof(struct Node));
   if(ptr==NULL)
   {       printf("OVERFLOW\n");
   }
   else
   {   ptr->data=data;
       if(head==NULL)
       {
           ptr->next=NULL;
           ptr->prev=NULL;
           head=ptr;
       }
       else
       {
          temp=head;
          while(temp->next!=NULL)
          {
              temp=temp->next;
          }
          temp->next=ptr;
          ptr->prev=temp;
          ptr->next=NULL;
        }
    }
}
void display()
{
    struct Node *temp=head;
    while(temp!=NULL)
    {
        printf("%d\n",temp->data);
        temp=temp->next;
    }
}
void delete()
{
    struct Node *temp=head;
    head=head->next;
    free(temp);
    printf("Node deleted from the begining\n");
}
int main() 
{
    struct node *head = NULL;  
    
insert(5);
insert(50);
insert(500);
display();
display();
delete();
display();
   
    

    return 0;
}

```

## Output:

<img width="428" height="335" alt="image" src="https://github.com/user-attachments/assets/817dc65e-dd99-4102-8d41-ebd51eb6c4bd" />


## Result: 

Thus, the function that deletes a given element from a linked list is verified successfully.
