# Stacks and Queues

## What is a Stack?
A stack is a structure made up of ```Nodes```. Each ```Node``` points to another ```Node``` but cannot point back to the previous one.

## Stack Terminology
- Push - Nodes or items that are put into the stack are pushed
- Pop - Nodes or items that are removed from the stack are popped. When you attempt to ```pop``` an empty stack an exception will be raised.
- Top - This is the top of the stack.
- Peek - When you ```peek``` you will view the value of the ```to```p Node in the stack. When you attempt to ```peek``` an empty stack an exception will be raised.
- IsEmpty - returns true when stack is empty otherwise returns false.

### Stack Ordering
- FILO - First In, Last Out: This means that the first item added in the stack will be the last item popped out of the stack.
- LIFO - Last In, First Out: This means that the last item added to the stack will be the first item popped out of the stack.

## What is a Queue?
A queue is a linear structure which follows a certain order for performing operations.

## Queue Terminology
- Enqueue - Nodes or items that are added to the queue.
- Dequeue - Nodes or items that are removed from the queue. If called when the queue is empty an exception will be raised.
- Front - This is the front/first Node of the queue.
- Rear - This is the rear/last Node of the queue.
- Peek - When you ```peek``` you will view the value of the ```front``` Node in the queue. If called when the queue is empty an exception will be raised.
- IsEmpty - returns true when queue is empty otherwise returns false.

### Queue Ordering
- FIFO - First In, First Out: This means that the first item in the queue will be the first item out of the queue.
- LILO - Last In, Last Out: This means that the last item in the queue will be the last item out of the queue.



[Table of Contents](README.md)