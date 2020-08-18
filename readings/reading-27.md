# Level Order Tree Traversal

## Refresher
Leverl order tree traversal is a common tree traversal method, but it is different from Pre-Order, In-Order, and Post-Order in a major way. This traversal is not oriented in from side to side, but top down. It is a breadth first traversal and it requires a little bit more complexity.

## Algorithm Logic
There are some notable restrictions in a tree that make this ordering difficult. For one, nodes are linked via the top down, so when trying to order from left to right at any level, there is no direct link. The only pathway to the other side of the tree is through the parent node. The other restriction is the fact that children cannot access their parents. The link is one-direction. The remedy this, an additional data structure comes in very handy to solve this issue. Enter the queue. As a node is visited, it is enqueued. Once enqueued, it can be dequeued. Upon this action, since we have access to it, we can enqueue its left child and then its right child. The front item in the queue would now be the root node's left child. As it is being dequeued, its own left and right children can be enqueued. This pattern provides a way for the the left and right brnaches of the tree to be re-accesssed and referenced in a top-down order that goes from left to right.

## Complexity
Since times are essentially referenced in order one after another, there is not inherent advantage to quickly finding a target value so the Time Complexity is O(n). The space complexity is is dependent on the addition of the queue data structure. The queue grows depending on if a dequeued node has the maximum of two children, so in a perfectly balanced tree, the Space Complexity is O(n).



[Table of Contents](../README.md)