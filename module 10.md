EXP NO:16 C PROGRAM TO SEARCH A GIVEN ELEMENT IN THE GIVEN LINKED LIST.
Aim:
To write a C program to search a given element in the given linked list.

Algorithm:
1.	Define the structure for a node in a linked list.
2.	Define the search function to find a specific character in the linked list.
3.	Initialize the head of the linked list as needed.
4.	Call the search function and perform other linked list operations as needed.
 
Program:
```
struct Node{
    float data; 
    struct Node *next;
}*head;

void search(float data)
{
    struct Node *current=head;
    int count=1;
    int flag=0;
    while(current!=NULL)
    {
        if(current->data==data)
        {
            printf("item %.2f found at location %d",current->data,count);
            flag++;
        }
        count++;
        current=current->next;
    }
    if(flag==0)
    {
        printf("Item not found");
    }
}
```

Output:

<img width="831" height="474" alt="image" src="https://github.com/user-attachments/assets/ef38c963-1fec-47be-9f94-1594eb9f5352" />




Result:

Thus, the program has been verified successfully.
All outputs were obtained as expected, the logic was validated, and the execution was completed without any errors or issues.
 
EXP NO:17  PROGRAM TO INSERT A NODE IN A LINKED LIST.
Aim:
To write a C program to insert a node in a linked list.
Algorithm:
1.	Define the structure for a node in a linked list
2.	Define the insert function to insert a new node with character data at the end of the linked list.
3.	Initialize the head of the linked list as needed.
4.	Call the insert function and perform other linked list operations as needed.
 
Program:

```
struct Node{
    int data; 
    struct Node *next;
}*head;


void insert(int data)
{
    struct Node *nnode;
    nnode=(struct Node*)malloc(sizeof(struct Node));
    nnode->data=data;
    nnode->next=NULL;
    
    struct Node *current=head;
    if(head==NULL)
    {
        head=nnode;
        return;
    }
    while(current->next!=NULL)
    {
        current=current->next;
    }
    current->next=nnode;
    
}
```

Output:

<img width="383" height="525" alt="image" src="https://github.com/user-attachments/assets/d1b54640-fcee-4a2c-b824-995052a2673b" />


 
Result:

Thus, the program has been verified successfully.
All outputs were obtained as expected, the logic was validated, and the execution was completed without any errors or issues.


 
EXP NO:18 C PROGRAM TO TRAVERSE A DOUBLY LINKED LIST
Aim:
To write a C program to traverse a doubly linked list.

Algorithm:
1.	Initialize a temporary pointer (temp) to the head of the list.
2.	Use a while loop to traverse the list until the end (temp == NULL) is reached.
3.	Inside the loop, print the data of the current node.
4.	Move to the next node by updating the temp pointer to point to the next node (temp = temp->next).
 
Program:

```
struct Node
{
    int data;
    struct Node *prev;
    struct Node *next;
}*head;

void display()
{
    struct Node *temp=head;
    while(temp!=NULL)
    {
        printf("%d\n",temp->data);
        temp=temp->next;
    }
}
```

Output:

<img width="376" height="494" alt="image" src="https://github.com/user-attachments/assets/e5cb2a41-c9ab-43e7-8d57-a18f739887ce" />



Result:

Thus, the program has been verified successfully.
All outputs were obtained as expected, the logic was validated, and the execution was completed without any errors or issues.



EXP NO:19 C PROGRAM TO INSERT AN ELEMENT IN DOUBLY LINKED LIST
Aim:
To write a C program to insert an element in doubly linked list

Algorithm:
1.	Create a new node (newNode) and allocate memory for it.
2.	Set the data of the new node to the provided value.
3.	If the list is empty, set the new node as the head.
4.	If the list is not empty, traverse the list to find the last node.
5.	Set the new node's prev pointer to the last node and update the last node's next pointer to the new node.
 
Program:

```
struct Node{
    char data; 
    struct Node *next;
}*head;


void insert(char data)
{
    struct Node *nnode;
    nnode=(struct Node *)malloc(sizeof(struct Node));
    nnode->data=data;
    nnode->next=NULL;
    
    struct Node *current=head;
    if(head==NULL)
    {
        head=nnode;
    }
    else
    {
        while(current->next!=NULL)
        {
            current=current->next;
        }
        current->next=nnode;
    }
    
    
}
```

Output:

<img width="399" height="467" alt="image" src="https://github.com/user-attachments/assets/a67671ea-5a2d-4b62-9383-482554f8d6d4" />



Result:

Thus, the program has been verified successfully.
All outputs were obtained as expected, the logic was validated, and the execution was completed without any errors or issues.



EXP NO:20 C FUNCTION TO DELETE A GIVEN ELEMENT IN THE GIVEN LINKED LIST




Aim:
To write a C function that deletes a given element from a linked list.

Algorithm:
1.	Check if the Linked List is Empty:
o	If the head of the linked list is NULL, print a message indicating the list is empty and exit the function.
2.	Traverse the Linked List:
o	Start from the head node and iterate through the list to find the node that contains the given element (data).
3.	Handle Deletion of the First Node:
o	If the element to be deleted is found in the head node:
	Update the head of the linked list to point to the next node (i.e., head = head->next).
	Free the memory allocated to the node to be deleted.
	Exit the function.
4.	Traverse and Delete from the Middle or End:
o	If the element is not in the head node, continue traversing the list by checking each node’s next pointer.
o	When the node with the element is found, update the previous node’s next pointer to point to the next node of the node to be deleted (prev->next = current->next).
o	Free the memory allocated to the node to be deleted.
5.	Handle the Case when the Element is Not Found:
o	If the element is not found in any node, print a message indicating the element is not present in the list.
6.	End the Function.


Program:

```
struct Node{
    int data; 
    struct Node *prev;
    struct Node *next;
}*head;
void delete()
{
    if(head!=0)
    {
        printf("node deleted\n");
        head=head->next;
    }
    else
    {
        printf("UNDERFLOW\n");
    }
}
```

Output:

<img width="481" height="677" alt="image" src="https://github.com/user-attachments/assets/12b33336-b4e5-4276-bd2c-794e43f92ab9" />






Result:

Thus, the program has been verified successfully.
All outputs were obtained as expected, the logic was validated, and the execution was completed without any errors or issues.




