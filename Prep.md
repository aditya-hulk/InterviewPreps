# About List Interface:
- A list in Java is a collection for storing elements in sequential order.
- Available in java.util package.
- public interface List<E> extends Collection<E>
## When to Use List?
- When we want to preserve my insertion order then we should go for list.
## About List (I)
- Duplicate elements are allowed (mutiple)
- null elements are allowed. (mutiple)
- It maintains insertion order. i.e. List can preserve the insertion order by using the index.
- Provide listIterator for iteration of element.
- In the list, we can add an element at any position. 
- Implementation classes are ArrayList, LinkedList, Vector, and Stack.
-  Various methods
    -  boolean add(Object o): 
    -  void add(int index, Object o):
    -  boolean addAll(Collection c): 
    - ListIterator listIterator()
    - etc... 

# About ArrayList
- Implementation class of List(I)
- Duplicate elements: Duplicate elements are allowed in the array list.
- Null elements: Any number of null elements can be added to ArrayList.
- Insertion order: It maintains the insertion order in Java. That is insertion order is preserved.
- Heterogeneous objects: Heterogeneous objects are allowed everywhere except TreeSet and TreeMap. Heterogeneous means different elements.
- Resizable-array: ArrayList is a resizable array or growable array that means the size of ArrayList can increase or decrease in size at runtime.
- Index-based structure: It uses an index-based structure in java.
- Synchronized: ArrayList is not synchronized. That means multiple threads can use the same ArrayList objects simultaneously.
- Implement Random Access, Serializable and Cloneble (I).
    - All are marker (I)
    - Random Access 
        -  we can access any random element at the same speed
        - Now assume that first element x can be accessed within only 1 sec.  Due to the implementation of random access interface, the 10th element and 1st crore element can also be accessed within 1 sec.
## About Advantage:
-  Dynamic size:
-  Easy to use : ArrayList is easy to use and provides a variety of methods for adding, removing, and accessing elements.
-   Type safety: ArrayList provides type-safety in Java, meaning that we can only add elements of the same data type.
## About disadvantage:
-  Performance: In ArrayList, manipulation is slow because if any element is removed from ArrayList, a lot of shifting takes place.
- Not thread-safe
- Not suitable for primitive types: 
## About Capacity
- ArrayList al = new ArrayList();
- It creates an empty ArrayList with a default initial capacity of 10.
- Once ArrayList is reached its maximum capacity, the ArrayList class automatically creates a new array with a larger capacity.
- New capacity = (current capacity*3/2) + 1 = 10*3/2 + 1 = 16

# About Vector
- Java Vector class is similar to ArrayList class with two main differences.
    - Vector is synchronized. It is used for thread safety.
    - It contains many legacy methods that are not now a part of the collections framework.
- The underlying Data structure for vector class is the resizable array or growable array.
- Duplicate elements are allowed
- Null elements are allowed
- insertion order is preserved
- Heterogeneous elements are allowed 
- methods of vector are synchronized. Two threads cannot access the same vector object at the same time
- Because of thread safety performance is poor.
- Vector is the best choice if the frequent operation is retrieval 
- Vector is created with an initial capacity of 10 but its size is increased by 100%.
    - i.e when vector reaches to it's full capacity it's new capacity will be doble of it's previous one.
    - eg initial capacity is 10 then new will be 20
# Difference between ArrayList and Vector in Java
![alt text](image-13.png)
# About Stack
- stack is a data structure that stores data in last-in, first-out fashion.
- This means an element that is stored as a last element into the stack, will be the first element to be removed from the stack.
- Only the top element on the stack is accessible at a given time.
- When an element (object) is inserted into the stack, it is called push operation.
- When an element is removed from the stack, it is called pop operation.
- Insertion and deletion of elements take place only from one side of the stack, traditionally called the top of the stack. 
- eg a stack of books, a stack of dvd
- Java Stack class extends vector class 
-  It implements List interface, RandomAccess , Serializable and Cloneable interfaces.
- Stack class is synchronized. That means it is thread-safe.
- Null elements are allowed into the stack.
- Duplicate elements are allowed into the stack.
-  E peek(): This method is used to retrieve the top-most element from the stack without removing it.
- Stack() constructor
# About Linked List
- Duplicate element are allowed.
- Null elements can be added 
- Heterogeneous elements are allowed
-  Java LinkedList is not synchronized. Therefore, It is not thread-safe. Since LinkedList is not synchronized. Hence, its operation is faster.
- Insertion and removal of elements in the LinkedList are fast because, in the linked list, there is no shifting of elements after each adding and removal.
- LinkedList is the best choice if your frequent operation is insertion or deletion in the middle
- Retrieval (getting) of elements is very slow in LinkedList because it traverses from the beginning or ending to reach the element.
- The underlying data structure of LinkedList is a doubly LinkedList data structure.
    - A doubly linked list consists of a group of nodes
    - Each node contains three fields: a data field that contains data stored in the node, left and right fields contain references or pointers that point to the previous and next nodes in the list.

![alt text](image-14.png)

- Java LinkedList class implements List, Deque, and Queue interfaces. It extends AbstractSequentialList. It also implements marker interfaces such as serializable and cloneable but does not implement random access interface.


