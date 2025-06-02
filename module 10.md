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
struct Node

{

     struct Node *prev;

    struct Node *next;

    float data;

}*head;



void search(float data)

{



    struct Node *temp;

    temp=head;

    float item=data;

    int i=0,flag;

    if(temp==NULL)

    {

         printf("List is empty");

    }

    else

    {

         while(temp!=0)

        {

             if(temp->data==item)

            {

                 printf("item %.2f found at location %d",item,i+1);

                flag=0;

            }i++;

             temp=temp->next;

         }

     }

     if(flag!=0)

     {

        printf("Item not found");

     }   

}
```

Output:

![437946687-c7cb6293-0f7a-4706-abdd-967706eceed8](https://github.com/user-attachments/assets/5a3e11f4-c2c8-47e6-9bc4-658e95e30856)




Result:
Thus, the program to search a given element in the given linked list is verified successfully.


 
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
   struct Node *ptr;
   ptr=(struct Node*)malloc(sizeof(struct Node));
   struct Node *temp;
   if(head==NULL){
      head=ptr;
      head->data=data;
      ptr->next=NULL;
      return;
  } 
  temp=head;
  while(temp->next!=NULL){
  temp=temp->next;
  }
  ptr->data=data;
  ptr->next=NULL;
  temp->next=ptr;
}
```

Output:

![437946813-247bcc84-7403-46d4-8a6c-a98bce2e6f27](https://github.com/user-attachments/assets/f3695ffe-5619-4b15-b1a0-8f553007debf)


 
Result:
Thus, the program to insert a node in a linked list is verified successfully.


 
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
    struct Node *prev;
    struct Node *next;
    int data;
}*head;

void display()
{
    while(head!=NULL)
    {
        printf("%d\n",head->data);
        head=head->next;
    } 
}
```
Output:

![437946943-1c279d3f-0641-44c0-9634-87063145fd3e](https://github.com/user-attachments/assets/bc124480-2d23-478f-86f2-2fa28aec49e4)


Result:
Thus, the program to traverse a doubly linked list is verified successfully. 



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
struct Node
{
    struct Node *prev;
    struct Node *next;
    char data;
}*head;

void insert(char data)
{
    struct Node *n=(struct Node *)malloc(sizeof(struct Node *));
    struct Node *temp;
    if(head==NULL)
    {
        head=n;
        head->data=data;
        n->next=NULL;
        return;
    }
    temp=head;
    while(temp->next!=NULL)
    {
        temp=temp->next;
    }
    n->data=data;
    n->next=NULL;
    temp->next=n;


}
```

Output:

![437947136-3fee65bc-c50b-4966-b4e5-ffec539a62e5](https://github.com/user-attachments/assets/6705c05f-c77e-4a5a-9599-145c610fb4c7)



Result:
Thus, the program to insert an element in doubly linked list is verified successfully.




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
struct Node
{
    char data; 
    struct Node *next;
}*head;
void delete()
{
    if(head != NULL)
    {
        head = head->next;
        printf("Node deleted from the begining ...\n");
    }
    else
   {
       printf("List is empty");
   }
}
```

Output:

![437947353-bc4417a1-7943-403f-aa48-6b353a7b6b2b](https://github.com/user-attachments/assets/4fd5f5b0-b58b-48b8-bd09-89be7b545db9)


Result:
Thus, the function that deletes a given element from a linked list is verified successfully.





