# Today I implemented the circular queue in C by referring the algorithms which are written by me.

## I got a bug while iterating the circular queue:
- I iterated the loop from front to rear.
- The condition I used to terminate the loop is i != rear+1.
- I updated the loop variable by i = (i+1) % SIZE.
- But whenever i reached rear+1 which is also equal to SIZE.
- Again i becomes 0 and the loop repeats into infinite loop.

## So, I solved it by updating i = (i+1) % SIZE+1.

## Here is the proof:
```C
#include <stdio.h>
#include <conio.h>
#define SIZE 20

int queue[SIZE], front = -1, rear = -1;

void enqueue(int element)
{
  if ((rear + 1) % SIZE == front)
  {
    printf("Queue is Overflow\n\n");
    return;
  }
  queue[(rear + 1) % SIZE] = element;
  rear = (rear + 1) % SIZE;
  printf("Enqueued: %d\n", queue[rear]);
  if (front == -1)
  {
    front = 0;
  }
  return;
}

void dequeue()
{
  if (front == -1 && rear == -1)
  {
    printf("Queue is Underflow\n\n");
    return;
  }
  else if (front == rear)
  {
    printf("Dequeued: %d\n", queue[front]);
    front = rear = -1;
    return;
  }
  else
  {
    printf("Dequeued: %d\n", queue[front]);
    front = (front + 1) % SIZE;
    return;
  }
}

void display()
{
  printf("Elements: ");
  for (int i = front; i != rear + 1; i = (i + 1) % (SIZE + 1))
  {
    printf("%d->", queue[i]);
  }
  printf("\n\n");
}

int main()
{
  int choice, element;
  while (1)
  {
    printf("\n\n1. Enqueue\n");
    printf("2. Dequeue\n");
    printf("3. Display\n");
    printf("4. Exit\n\n\n");
    printf("Enter the choice: ");
    scanf("%d", &choice);

    switch (choice)
    {
    case 1:
      printf("Enter an element: ");
      scanf("%d", &element);
      enqueue(element);
      break;
    case 2:
      dequeue();
      break;
    case 3:
      display();
      break;
    case 4:
      return 0;
    }
  }
  return 0;
}
```
