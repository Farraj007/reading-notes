[Main Page](../README.md)

# Reading Notes 30  

## KEY NOTES

Hash maps do this to store vlaues:
- accept a key
- calculate the hash of the key
- use modulus to convert the has into an array index  
- store the key with the value by appending both to the end of a linked list  

Hash maps do this to read a value:  
- accept a key  
- calculate the has of the key  
- use modulus to convert the hash into an array index  
- use the array index to access the short LinkedList representing a bucket   
- search through the bucket looking for a node with a key/value pair that matches the key you were given.  

Internal methods of a hashtable  

- add()
    - Adds a new key/value pair to the table  
- find()
    - Finds a key/value pair  
- contains()
    - Boolean if a key/value pair exists  
- GetHash()
    - Takes a key as a string, conducts a hash, and returns the index value.
