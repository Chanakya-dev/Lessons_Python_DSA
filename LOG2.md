# Video Based Questions

## Array Basics in Data Structures - MCQs

### **1. What is an array in Data Structures?**
- a) A collection of elements of different data types stored at contiguous memory locations.
- b) A collection of elements of the same data type stored at contiguous memory locations.
- c) A collection of pointers to elements stored randomly in memory.
- d) A list of key-value pairs.

**Answer:** b) A collection of elements of the same data type stored at contiguous memory locations.

---

### **2. What is the index of the first element in an array in most programming languages?**
- a) -1
- b) 0
- c) 1
- d) Depends on the language

**Answer:** b) 0

---

### **3. What is the time complexity of searching for an element in an unsorted array using linear search?**
- a) \( O(1) \)
- b) \( O(\log n) \)
- c) \( O(n) \)
- d) \( O(n^2) \)

**Answer:** c) \( O(n) \)

---

### **4. Which of the following operations is not efficient in an array?**
- a) Accessing an element by its index.
- b) Inserting an element at the end.
- c) Deleting an element from the middle.
- d) Iterating through the array.

**Answer:** c) Deleting an element from the middle.

---

### **5. If an array has 10 elements, what is the index of the last element?**
- a) 9
- b) 10
- c) 11
- d) Undefined

**Answer:** a) 9

---

### **6. Which of the following statements about arrays is correct?**
- a) Arrays can dynamically change their size during runtime.
- b) Array size must be defined at compile time in statically-typed languages.
- c) Arrays always require less memory than linked lists.
- d) Elements in an array can only be accessed sequentially.

**Answer:** b) Array size must be defined at compile time in statically-typed languages.

---

### **7. What is the time complexity of inserting an element at a specific position in an array?**
- a) \( O(1) \)
- b) \( O(\log n) \)
- c) \( O(n) \)
- d) \( O(n^2) \)

**Answer:** c) \( O(n) \)

---

### **8. Which of the following can be used to initialize an array in Python?**
- a) `arr = [1, 2, 3, 4, 5]`
- b) `arr = [0] * 5`
- c) `arr = array('i', [1, 2, 3])` *(using the `array` module)*
- d) All of the above

**Answer:** d) All of the above
---

### **9. What is the time complexity of searching for an element in a sorted array using binary search?**
- a) \( O(1) \)
- b) \( O(\log n) \)
- c) \( O(n) \)
- d) \( O(n^2) \)

**Answer:** b) \( O(\log n) \)

---

### **10. What is the time complexity of inserting an element at the beginning of an array?**
- a) \( O(1) \)
- b) \( O(\log n) \)
- c) \( O(n) \)
- d) \( O(n^2) \)

**Answer:** c) \( O(n) \)

---

### **11. What is the time complexity of deleting an element from the end of an array?**
- a) \( O(1) \)
- b) \( O(\log n) \)
- c) \( O(n) \)
- d) \( O(n^2) \)

**Answer:** a) \( O(1) \)

---
## LinkedList
## Insert at Front

### 1. Implement the insert_at_beginning method in a LinkedList class. You are provided with an input sequence of integers. Insert them into the linked list at the beginning, and then return the final linked list.

> Input:
- 4
- 3 5 7 9
> Ouput: 
- 9 --> 7 --> 5 --> 3 --> None

### 2. Fill Out The Code Snippet
```python
class Node:
    def _init_(self, data):
        self.data = data
        self.next = None

class LinkedList:
    def _init_(self):
        self.head = None
    def insert_at_beginning(self, data):
        //Fill Out Your Code Here
        self.head = new_node
```
### 3.What is the time complexity of the insert_at_beginning operation?
- a) O(1)
- b) O(n)
- c) O(log n)
- d) O(n^2)

**Answer:** a) O(1)


## Insert at End

### Problem Statement:
1) The following `insert_at_end` method contains two bugs:  
1. It does not handle the case when `self.head` is `None`.  
2. It tries to assign `current.next` when `current` itself could be `None`.  

### Code with Bugs:
```python
def insert_at_end(self, data):
    new_node = Node(data)
    current = self.head  # Bug: What happens if self.head is None?
    while current and current.next:
        current = current.next
    current.next = new_node  # Bug: May throw an error if current is None
```
### Question:
2) In the `insert_at_end` method, what is the purpose of the `while current.next:` loop?

### Options:
1. To find the head of the linked list.  
2. To traverse the linked list until the last node.  
3. To insert the new node in the middle of the list.  
4. To check if the list is circular.  

### Correct Answer:
2. To traverse the linked list until the last node.

---

### Question:
3) Complete the following code for the `insert_at_end` method:

```python
def insert_at_end(self, data):
    new_node = Node(data)
    if not self.head:
        self.head = new_node
        return
    current = self.head
    while ____________________________:
        ____________________________
    ____________________________
```
Answer Snippet
```python
def insert_at_end(self, data):
    new_node = Node(data)
    if not self.head:
        self.head = new_node
        return
    current = self.head
    while current.next:
        current = current.next
    current.next = new_node
```
## Deleting Nodes

### Bug Fix: Deleting a Node from Linked List

### Problem Statement:
The `delete_node` method below contains bugs that need to be fixed:  
1. It doesn't handle the case where the list is empty (`self.head` is `None`).  
2. It doesn't handle the case where the node to be deleted is the head node.

```python
def delete_node(self, key):
    current = self.head
    while current and current.data != key:
        prev = current
        current = current.next
    prev.next = current.next  # Bug: What happens if current is None?
```

### Fixed Code:
```python
def delete_node(self, key):
    if not self.head:  # Handle case where list is empty
        print("List is empty")
        return
    
    if self.head.data == key:  # Handle case where the head is the node to be deleted
        self.head = self.head.next
        return

    current = self.head
    prev = None
    while current and current.data != key:
        prev = current
        current = current.next
    
    if not current:  # Node with the key doesn't exist
        print("Key not found in the list")
        return
    
    prev.next = current.next
```

---

### MCQ: Deleting Nodes from Linked List

### Question 1:
What does the following code do?  

```python
if self.head.data == key:
    self.head = self.head.next
```

#### Options:
1. Deletes the tail of the linked list.  
2. Deletes the first node with the given key if it is the head.  
3. Deletes all nodes with the given key.  
4. Does nothing if the key is not found.  

#### Correct Answer:
2. Deletes the first node with the given key if it is the head.

---

### Question 2:
What happens if the `delete_node` method is called with a key that does not exist in the list?

#### Options:
1. It throws an error.  
2. It deletes a random node.  
3. It traverses the entire list but does not delete anything.  
4. It resets the list to empty.  

#### Correct Answer:
3. It traverses the entire list but does not delete anything.

---

## Code Completion: Deleting a Node

### Question:
Complete the following code for the `delete_node` method in a linked list:

```python
def delete_node(self, key):
    if not self.head:
        ____________________________
        return
    
    if self.head.data == key:
        ____________________________
        return
    
    current = self.head
    prev = None
    while ____________________________:
        ____________________________
    
    if not current:
        ____________________________
        return
    
    ____________________________
```

### Answer:
```python
def delete_node(self, key):
    if not self.head:
        print("List is empty")
        return
    
    if self.head.data == key:
        self.head = self.head.next
        return
    
    current = self.head
    prev = None
    while current and current.data != key:
        prev = current
        current = current.next
    
    if not current:
        print("Key not found in the list")
        return
    
    prev.next = current.next
```

---

## Code Writing Challenge: Deleting the Entire Linked List

### Question:
Write a method to delete all nodes in a linked list.

### Answer:
```python
def delete_list(self):
    self.head = None
    print("Linked list deleted")
```

---

