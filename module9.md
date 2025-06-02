EXP NO:11 C PROGRAM TO DISPLAY STACK ELEMENTS USING AN ARRAY.

Aim:
To write a C program to display stack elements using an array.
Algorithm:
1.	Include Necessary Header Files
2.	Declare Global Variables
3.	Define the Display Function
4.	Main Function (or Other Relevant Code)
5.	Initialize the stack and top as needed.
6.	Perform stack operations (push, pop, etc.).
7.	Use the display function to visualize the stack's contents
 
Program:
```
float stack[50];
int top,i;
void display()
{
    for(i = top; i >= 0; i--)
    {
        printf("%.1f ",stack[i]);
    }
}
```

Output:

![437943899-ac44ce4a-4870-4af9-889c-96ed85b8569b](https://github.com/user-attachments/assets/604e846e-3f06-47e9-bb91-8cf88ed348bd)




Result:
Thus, the program to display stack elements using an array is verified successfully.
 

EXP NO:12  PROGRAM TO PUSH THE GIVEN ELEMENT IN TO A STACK USING ARRAY.


Aim:
To create a C program to push the given element in to a stack using array.
Algorithm:
1.	Declare global variables for the stack size, top index, and the stack itself.
2.	Define the push function to add a floating-point number to the stack.
3.	Initialize the stack size, top index, and the stack itself.
4.	Call the push function as needed.
 
Program:
```
int size=3;
float stack[100];
int top=-1;
void push(float data)
{
    if(top==size-1)
    {
        printf("stack is full\n");
    }
    else
    {
        top++;
        stack[top]=data;
    }
}
```

Output:


![437944407-f43802a2-6af6-4c91-bfd7-cc996d705061](https://github.com/user-attachments/assets/89e79070-7b47-490f-9bb5-7d5b7cfc823f)




Result:
Thus, the program to push the given element in to a stack using array is verified successfully


 
EXP NO:13 C PROGRAM TO DISPLAY QUEUE ELEMENTS USING ARRAY.


Aim:
To write a C program to display queue elements using array

Algorithm:
1.	Declare global variables for the queue, rear, front, and iteration.
2.	Define the display function to print the elements of the queue.
3.	Initialize the queue, rear, and front as needed.
4.	Call the display function and perform other queue operations as needed.
 
Program:
```
int rear,front;
int i;
char queue[50];
void display()
{
    if(rear==-1&&front==-1)
    {
    printf("No elements to display");
    }
    else
    {
        for(i=front;i<=rear;i++)
        {
            printf("%c\n",queue[i]);
        }
    }
}
```

Output:

![437944666-0b751430-e9e4-4c77-b1c5-f4034499983e](https://github.com/user-attachments/assets/a844213f-bbfd-426f-908b-4c6743c60a50)



Result:
Thus, the program to display queue elements using array is verified successfully.


 
EXP NO:14 C PROGRAM TO INSERT ELEMENTS IN QUEUE USING ARRAY.


Aim:
To write a C program to insert elements in queue using array.

Algorithm:
1.	Declare global variables for the size, rear, front, and the queue itself.
2.	Define the enqueue function to add a float to the queue.
3.	Initialize the rear, front, and size of the queue as needed.
4.	Call the enqueue function as needed.

Program:
```
int size=10,rear=-1,front=-1;
float queue[50];
void enqueue(float data)
{
    if(rear<size)
    {
        if(front==-1)
        {
            front=0;
        }
        rear++;
        queue[rear]=data;
    }
}
```

Output:

![437944936-af2108b5-c8df-44ac-9947-e7d0f3effa1a](https://github.com/user-attachments/assets/978236e6-43b4-49e8-84cd-f946a06ea90d)


Result:
Thus, the program to insert elements in queue using array is verified successfully.



 
EXP NO:15 C FUNCTION TO DELETE ELEMENTS IN QUEUE USING ARRAY



Aim:

To create a function in C that deletes an element from a queue implemented using an array.

Algorithm:

1.	Check if the Queue is Empty
o	If the front pointer is -1, it means the queue is empty, and there are no elements to delete. Print a message indicating that the queue is empty.
2.	Delete the Front Element
o	If the queue is not empty, the element at the front index is deleted.
o	Increment the front pointer by 1 to remove the element and point to the next element in the queue.
3.	Check if the Queue Becomes Empty After Deletion:
o	After deletion, check if the front pointer has passed the rear pointer (front > rear). If this is true, reset both front and rear to -1, indicating that the queue is now empty.
4.	End the Function.



Program:
```
int front, rear;
void dequeue()
{
    if(front == -1 || front>rear)
    {
        printf("Queue Underflow.\n");
        return;
    }
    else
    {
        front=front+1;
    }
}
```

Output:


![437945129-2acaa16d-5670-4bb0-b009-5fa0f4692a6e](https://github.com/user-attachments/assets/bf4604ea-f0fa-4cd0-bfaf-8f0e61f73307)


Result:
Thus, the function that deletes an element from a queue implemented using an array is verified successfully.
