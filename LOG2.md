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

## Searching for Nodes

---

### Bug Fix: Searching for a Node

### Problem Statement:
The following `search` method contains issues:  
1. It does not account for an empty linked list.  
2. It assumes the node will always be found, leading to potential errors.

```python
def search(self, key):
    current = self.head
    while current.data != key:  # Bug: What happens if current is None?
        current = current.next
    return current
```

### Fixed Code:
```python
def search(self, key):
    current = self.head
    while current:
        if current.data == key:
            return current
        current = current.next
    return None  # Return None if the key is not found
```

---

### MCQ: Searching for Nodes

### Question 1:
What is the time complexity of the `search` method in a singly linked list?

#### Options:
1. \( O(1) \)  
2. \( O(\log n) \)  
3. \( O(n) \)  
4. \( O(n^2) \)  

#### Correct Answer:
3. \( O(n) \)

---

### Question 2:
What happens if the `search` method is called with a key that is not in the linked list?

#### Options:
1. It returns the head of the list.  
2. It returns the last node.  
3. It traverses the entire list and returns `None`.  
4. It throws an error.  

#### Correct Answer:
3. It traverses the entire list and returns `None`.

---

### Code Completion: Searching for a Node

### Question:
Complete the following code for the `search` method in a linked list:

```python
def search(self, key):
    current = self.head
    while ____________________________:
        if ____________________________:
            ____________________________
        current = ____________________________
    return ____________________________
```

### Answer:
```python
def search(self, key):
    current = self.head
    while current:
        if current.data == key:
            return current
        current = current.next
    return None
```

---

### Code Writing Challenge: Finding a Node’s Position

### Question:
Write a method to return the position (0-based index) of the first occurrence of a given key in a linked list. Return `-1` if the key is not found.

### Answer:
```python
def find_position(self, key):
    current = self.head
    position = 0
    while current:
        if current.data == key:
            return position
        current = current.next
        position += 1
    return -1  # Return -1 if the key is not found
```

# Doubly Linked List

## Insert at Front Questions

### 1. Basic Insert at Front
**Problem:** Write the `insert_at_front` method to insert a new node at the front of the doubly linked list.

```python
def insert_at_front(self, data):
    new_node = Node(data)
    ____________________________
```
**Answer**
---
def insert_at_front(self, data):
    new_node = Node(data)
    new_node.next = self.head
    if self.head:
        self.head.prev = new_node
    self.head = new_node

### 2. Insert at Front with Empty List
- **Problem:** What happens if you call insert_at_front on an empty list?

**Answer:** The new node should be inserted and become the head of the list. No prev pointer update is needed if the list is empty.

```python
def insert_at_front(self, data):
    new_node = Node(data)
    if not self.head:
        self.head = new_node
        return
    new_node.next = self.head
    self.head.prev = new_node
    self.head = new_node
```
### 3. Insert at Front with Multiple Nodes
- **Problem:** Write a method to insert a new node at the front when the list already has several nodes. Make sure that the new node becomes the first node and its prev pointer is set to None.

```python
def insert_at_front(self, data):
    new_node = Node(data)
    new_node.next = self.head
    if self.head:
        self.head.prev = new_node
    self.head = new_node
    new_node.prev = None
```
### 1) Insert at End

- ** Problem:** Write the insert_at_end method to insert a new node at the end of the doubly linked list.

```python
def insert_at_end(self, data):
    new_node = Node(data)
    ____________________________
```
### 2) Insert at End in Empty List

- ** Problem:** What happens if you try to insert a node at the end of an empty list? How would you handle it?
- **Answer:** When the list is empty, the new node should be inserted as the head of the list.
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
    new_node.prev = current
```
### 3) Insert at End with Multiple Nodes
- **Problem:** Write a method to insert a new node at the end when there are already multiple nodes in the doubly linked list.
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
    new_node.prev = current
```
## Delete Node at First

### 1) Delete the First Node in a Doubly Linked List
- **Problem:** Write a function to delete the first node (head node) in a doubly linked list.

```python
def delete_first(self):
    if self.head is None:
        return  # List is empty
    if self.head.next is None:  # Only one node in the list
        self.head = None
    else:
        self.head = self.head.next
        self.head.prev = None
```

### 2) Delete the Last Node in a Doubly Linked List
**Problem:** Write a function to delete the last node (tail node) in a doubly linked list.
```python
def delete_last(self):
    if self.head is None:
        return  # List is empty
    if self.head.next is None:  # Only one node in the list
        self.head = None
    else:
        self.tail = self.tail.prev
        self.tail.next = None
```
### 3) Fill the Following Code Snippet and Complete The Delete at End Logic
- **Description:** This function deletes a node at a End in the doubly linked list.
```python
def delete_at_end(self):
    if self.head is None:  # If the list is empty
        print("List is empty!")
        return

    if self.head == self.tail:  # If there's only one node
        self.head = self.tail = None
    else:
        #\Write the code to move the tail to the previous node
        #Write the code to set the new tail's next pointer to None
        pass
```
### 4) Delete Node at a Specific Index
- **Description:** This function deletes a node at a specific index in the doubly linked list.

```python
def delete_at_index(self, index):
    // Fill Out Your Code Here     
    pass
```
### **MCQ 1: Deleting Node at the Front**

**Question:**  
What happens when you delete the front node of a doubly linked list?

**Options:**
1. The `head` pointer is set to `None` without modifying the `prev` of the next node.
2. The `head` pointer is updated to point to the next node, and the new head’s `prev` pointer is set to `None`.
3. The `tail` pointer is updated to point to the previous node.
4. The `head` pointer is updated, but the `next` pointer of the old head is not removed.

**Correct Answer:** 2. The `head` pointer is updated to point to the next node, and the new head’s `prev` pointer is set to `None`.

---

### **MCQ 2: Deleting Node at the End**

**Question:**  
What happens when you delete the node at the end of a doubly linked list?

**Options:**
1. The `tail` pointer is set to `None` without modifying the `next` pointer of the previous node.
2. The `tail` pointer is updated to the previous node, and the new tail’s `next` pointer is set to `None`.
3. The `head` pointer is updated to the previous node.
4. The node before the last node is removed from the list.

**Correct Answer:** 2. The `tail` pointer is updated to the previous node, and the new tail’s `next` pointer is set to `None`.

---

### **MCQ 3: Deleting Front Node in an Empty List**

**Question:**  
What happens when you try to delete the front node in an empty doubly linked list?

**Options:**
1. The function throws an exception.
2. The `head` and `tail` pointers are both set to `None`.
3. Nothing happens; the function just returns.
4. The `head` pointer is set to `None` without changing `tail`.

**Correct Answer:** 1. The function throws an exception.

---

### **MCQ 4: Deleting Node from Front in a Single Node List**

**Question:**  
What happens when you delete the front node in a doubly linked list that has only one node?

**Options:**
1. Both `head` and `tail` pointers are set to `None`.
2. The `head` pointer is set to `None`, but `tail` remains unchanged.
3. The `tail` pointer is updated to `None`, but `head` remains unchanged.
4. The list remains unchanged.

**Correct Answer:** 1. Both `head` and `tail` pointers are set to `None`.

---

### **MCQ 5: Edge Case in Deleting at the End**

**Question:**  
If the doubly linked list has only one node, what happens when you attempt to delete the node at the end?

**Options:**
1. Both `head` and `tail` are set to `None`.
2. The node is removed, but the list remains unchanged.
3. Only the `head` pointer is updated to `None`.
4. An error is raised because the list has only one node.

**Correct Answer:** 1. Both `head` and `tail` are set to `None`.

---

### **MCQ 6: After Deleting the Front Node**

**Question:**  
What should be done after deleting the front node in a doubly linked list?

**Options:**
1. The `head` pointer should point to the next node, and the `next` pointer of the new head should point to `None`.
2. The `head` pointer should point to the next node, and the `prev` pointer of the new head should be set to `None`.
3. The `next` pointer of the deleted node should be set to `None`.
4. The list remains unchanged except for the node being deleted.

**Correct Answer:** 2. The `head` pointer should point to the next node, and the `prev` pointer of the new head should be set to `None`.

---

### **MCQ 7: Deleting the Last Node in a Multi-Node List**

**Question:**  
When deleting the last node in a doubly linked list, what happens to the `tail` pointer?

**Options:**
1. The `tail` pointer points to the second-last node, and its `next` pointer is set to `None`.
2. The `tail` pointer remains unchanged, and the list has no end.
3. The `tail` pointer is deleted along with the last node.
4. The `tail` pointer points to `None` after the last node is deleted.

**Correct Answer:** 1. The `tail` pointer points to the second-last node, and its `next` pointer is set to `None`.

---

### **MCQ 8: Deleting Node at Front with Multiple Nodes**

**Question:**  
What happens when you delete the front node in a doubly linked list with multiple nodes?

**Options:**
1. The `head` pointer moves to the next node, and the new head’s `prev` pointer is set to `None`.
2. The list becomes empty, and both `head` and `tail` are set to `None`.
3. The list remains unchanged except for the removed front node.
4. The `next` pointer of the old head is set to `None`.

**Correct Answer:** 1. The `head` pointer moves to the next node, and the new head’s `prev` pointer is set to `None`.

## Doubly LinkedList Search
### 1) Complete the following function to search for a value in a doubly linked list.

```python
def search(self, key):
    current = self.head
    while current:
        if current.data == key:
            return True  # Return True if the element is found
        current = current.next
    return False  # Return False if the element is not found
``` 
### 2) There is a bug in the following code. Identify and fix the issue in the search function.

```python
def search(self, key):
    current = self.head
    while current:
        if current.data == key:
            print("Found!")
        current = current.next
    print("Not Found!")
```
### 3) What is the time complexity of searching for a node in a doubly linked list with n nodes?
**1)** O(1)
**2)** O(log n)
**3)** O(n)
**4)** O(n^2)

- **Answer:** 3. O(n)
