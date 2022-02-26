[:arrow_backward:](../README.md)
## Pain and Suffering
[Pain vs Suffer](https://codefellows.github.io/code-401-python-guide/curriculum/class-01/notes/pain_suffering)  

Suffering is just a mental /physical pain without  paying off . pain will pay of if you have a goal ambition and grit.  
**As you go through pain ask yourself these questions**  
1-What’s your perspective?  
2-Why are you doing this?  
3-Do you want what comes at the end of this journey?  
4-Are you doing this for you?

`seek the remedy!` Ask questions that bridge the gap between what you know and what you need to be able to do. 

# Beginners Guide to the Big O
 [Link to Article](https://rob-bell.net/2009/06/a-beginners-guide-to-big-o-notation/)  

### Big O Notation

**Big O Notaion** is used in Computer Science to describe performance or complexity of an algorithm.  
 - `O(1)` describes an algorithm that will always execute in the same time (or space) regardless of the size of the input data set.  
 - `O(N)` describes an algorithm whose performance will grow linearly and in direct proportion to the size of the input data set.  
 - `O(N^2)` represents an algorithm whose performance is directly proportional to the square of the size of the input data set. 
    - Common with algorithms involving nested iterations.
    - Deeper nested iterations will result in O(N^3), and O(N^4) 
 - `O(2^N)` denotes an algorithm whose growth doubles with each additon to the input data set.   

#### Logarithms  

`Binary search`: is a technique used to search sorted data sets. It works by selected a middle value, a median and compares it to a target value.  
- if a match returns success.  
- if target is > than median splits data set taking upper half.
- if target is < than median splits data set taking lower half.  
- Does this until it reaches a match or can't split anymore.  

This type of algorithm is described as `O(logN)`.  
- This produces a growth curve that peaks at the beginning and flattens out as the size of the data sets increase. For example:
    - Data set with 10 items = 1 second run time.  
    - Data set with 100 items = 2 second run time.  
    - Data set with 1000 items = 3 second run time.  
Increasing size has little effect on its growth. Making this type of algorithm extremely effecient when dealing with large data sets.