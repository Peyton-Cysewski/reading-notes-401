# Linked Lists

## What is a Linked List?
A linked list is sequence of nodes that are linked. Each node has a value (since it is a list), and points to the next node in the list.

#### Parts
- Node: One 'link' in the 'chain' of the linked list.
- Next: A property that references the next node.
- Head: A reference type of type node that points to the first node of a linked list.
- Current: A reference type of type node that refers to the current node being looked at.

#### Types of Lists
- Singly: The nodes of this type of list only has one reference which points to the next node.
- Doubly: The nodes of this type of list have two references; next points forward to the next node and previous points backwards to the previous node.

#### Traversal
Since you are not able to use for or foreach loops with linked lists, the best way to loop through the list is with a while loop and at the end of each loop have the current value be changes to next so the upcoming loop points to the next node in the list..

## More About Linked Lists
- Linked lists are a linear type of data structure.
- Memory does not need to be contiguous since each value can point to another place in memory.
- Dynamic in nature (arrays are static).
- Although odd, linked lists can be made into circular lists as well.
- Most useful in instances where you either don't know the size of a list, or want to change it's overall size dynamically.



[Table of Contents](../README.md)
