# Hash Tables

## What is a Hash Table?
To begin, it is important to note that a hash is the output of some input after it is put through a specific algorithm. This can be done for security purposes, or in this case, to get a value that will be used in the same way an index is used in an array. Each index of a hash table has a bucket to store values. This is because there is the potential for a collison to occur meaning that multiple values could be at the same part of the array. Lastly, a collison is what happens when two values get assigned the same hash. In essence they collide at the same point in the table.</br>
Common Methods for Hash Tables include:
- `Add`: Adds a new key/value pair to the hash table.
- `Find`: Takes in a key and ultimately returns the assocaited value.
- `Contains`: Returns a bool based on whether an input key have a value in the table.
- `GetHash`: Hashes an input key and returns the value (same as the array index).

## Other Info
- Time Complexity: O(1)
- Space Complexity: O(n)
- Useful for large data sets that need to be accessed quickly.
- The ideal hash map has not collisions, but if it has to have them, then the collisons woudl be equally distributed.
- There are several techniques for effective hashing, but all should use prime numbers to help with collsion distribution.
- If an array cannot have collision or deal with them via linked lists, then one alternative method is to use linear probing (also known as open addressing). The probing algorithms are commonly linear, exponential, or incorporate a second hash value.



[Table of Contents](README.md)