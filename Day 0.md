## Day 0
1. Use cases of Lists -  
   Student marks - updating, deleting, editing  
   Shopping cart - adding, removing  
   To do list (Notion)  
   Playlist - creating a queue  
   Multi-dimensional data  

   Use cases of tuples -  
   Date of Birth - (17,04,2006)  
   Employee ID details  
   Prices of goods in shops (fixed value)  
   Past money transcactions  

2. Time complexity, Search complexity -  
   Lists:  
   Search - always O(n)   
   Insertion at beginning/position - list.insert(0,x) - O(n)  
   Appending at end - list.append(x) - O(1)  
   Deletion at end - list.pop() - O(1)  
   Deleting at beginning/position - list.pop(i) - O(n)  
   Deletion using value - list.remove(x) - O(n)  

   Tuples:  
   Accessing an element - O(1)  
   Searching - always O(n)  
   Appending - creating a new tuple and adding - O(n)  
   Deleting - slicing - O(n)  
 
3. Sort used in list.sort()  
   Timsort - created by Tim Peters  
   A combination of Merge sort + Insertion sort  
   Stable sort   
   Best case - O(n)  
   Worst case - O(n log n)  
   Approach:  
   Divides the array into small "runs" - either in asc, desc, or reversed small arrays  
   Fixes small runs like reversed array - [2,1] -> [1,2] using insertion sort  
   Merges smaller runs - using merge sort  
   sorted() - also uses Timsort but returns a new list  

## Problem Sheet:

1.Counting sort works best for this situation  
   - Since it is a fixed range, non-comparison sorts like counting or radix sort work better  
   - Comparison sort - Best case - O(n log n)  
   - Non-comparison sort - o(n x k), here - O(8 x n) - O(n), works best  
   - Lower bound - O(n)  
   - Upper bound - O(n x k)
  
2.Factorial for large numbers:  
   - Store every digit as an element in an array in reverse order  
   - 15!, every digit of the factorial is stored as an element  
   - Numbers not natively supported by computer can be represented this way  
  
3.1,00,000(30ms+0.01ms) (assuming it fits into primary storage)  
   1,00,000(30.01)  
   30,01,000ms=3001s
   =50.01 mins

 4.Integer addition & subtraction - fastest, 1 CPU cycle  
   Integer multiplication - slower compared to integer addition and subtraction  
   Floating point - very slow cause it has to follow IEEE 745 precision, normalization rules  

5.Hash table works best  
   - O(1) - time complexity  
   - uses less memory  
   - can be used for exact matching
     
  Tries could also be used  
   - uses more memory  
   - can be used for searching using prefix  
   - O(L) - time complexity where L-length of prefix  

6. For arbitrary set of inputs, sort the array, choose the middle element as root and build the tree  
   Balanced tree - lesser height - faster operations - O(log n)   
   AVL tree more balanced than Red-Black trees

7. pop() and top() are not combined as it will reduce it's efficiency  
   pop() - in some implementations does not return value, whereas top() only views element  
   combining increases time complexity

8. MST real life applications -  
   Road - highway planning connecting minimum distances    
   Rail - train track planning using least distances  

   10.Fibonacci series -  
    Without dynamic programming: Recursion is used, Time complexity becomes O(2^n), overlapping occurs  
    With dynamic programming: No overlapping occurs, every condition run exactly once, therefore time complexity - O(n)  

    12.Object Serialization -  
    Process of converting object into byte stream to either save to a file, to store in a database or to transmit over a network  
    No, any object cannot be serialized  
    In python, import pickle -> cause it knows how to store its internal structure for data types like integer, string  
    Functions cannot be serialized, as they are executed at a particular time  

    13.Sleep -
    CPU turns off  
    RAM is on  
    RAM preserves the state in which the laptop was finally  

    Hibernate -
    CPU turns off  
    Copies RAM contents and stores it as an image in a disk  
    CPU registers, kernel state, page tables are used to reconstruct the last system state from the image stored  

    Limitations of sleep -  
    If battery dies, RAM state is lost  
    Same way, if USB devices are removed, information is lost  

    Limitations of hibernate -  
    Drivers may not support after hibernation  
    External monitors may fail to reconnect directly  


   





   
