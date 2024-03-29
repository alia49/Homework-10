# Homework-10
Sudo Code:
Define a TreeNode structure with:
    - An integer value
    - A left child node
    - A right child node

Function levelOrder takes a TreeNode root and returns a list of lists of integers:
    Initialize an empty list of lists, result
    
    If root is null:
        Return result
    
    Initialize a queue and enqueue the root node
    
    While the queue is not empty:
        Determine the number of nodes at the current level, levelNum
        
        Initialize an empty list, subList, for this level's values
        
        For each node at this level (i from 0 to levelNum - 1):
            Peek at the front node in the queue (but do not dequeue yet)
            
            If the front node has a left child:
                Enqueue the left child
                
            If the front node has a right child:
                Enqueue the right child
                
            Dequeue the front node and add its value to subList
        
        Add subList to result
    
    Return result

Main program:
    Construct a binary tree manually:
        Create a root node with value 4
        Add left child with value 3 and right child with value 8 to the root
        Add children to the node with value 3: left child with value 1, right child with value 5
        Add a right child with value 9 to the node with value 8
        
    Call levelOrder with the root of the tree
    
    Print the result

