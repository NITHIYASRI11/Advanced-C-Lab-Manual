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
int stack[100],top=-1,i;
void display()
{
    if(top==-1){
           printf("stack is empty\n");
    } 
    else{
       
    for(i=top;i>=0;i--)
    {
        
        printf("%d->",stack[top--]);
    }
    }
}

```
Output:

![image](https://github.com/user-attachments/assets/1dbf0fba-9882-48a0-b774-6ee5d58c6f19)




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
int size=3,top=-1;
float stack[100];
void push (float data)
{
    if (top == size )
    {
    printf("stack is full\n");
    }
    else
    {
        top = top +1;
        stack[top] = data;
    }
}
```
Output:

![image](https://github.com/user-attachments/assets/454e15f6-5fa6-4425-891d-b541eb1aeda1)





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
float queue[50];
int rear=-1, front=-1;
void display()
{
    int i=0;
    if((front=-1)&&(rear==-1))
    printf("No elements to display\n");
    else
    {
        for(i=front+1;i<=rear;i++)
        {
            printf("%.1f\n", queue[i]);
        }
    }
}
```

Output:

![image](https://github.com/user-attachments/assets/0f330dbd-9b03-4cd4-bb6b-9f6456a2c996)



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
int size=3, rear=-1, front=-1;
float queue[50];
void enqueue(float data)
{
    if(rear==-1&&front==-1){
        front=0;
        rear=0;
        queue[rear]=data;
    }
    else
    {
        rear=(rear+1)%size;
        queue[rear]=data;
    }
}

```

Output:

![image](https://github.com/user-attachments/assets/a72340eb-fa7e-4c3a-a5d6-537d51152630)


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
    if((front=-1)&&(rear==-1))
    {
        printf("Queue is empty");
       
    }
    else
    {
        front=front+2;
    }
}
```

Output:

![image](https://github.com/user-attachments/assets/a28ce940-723b-44d7-be3f-4de73fd929ff)



Result:
Thus, the function that deletes an element from a queue implemented using an array is verified successfully.
