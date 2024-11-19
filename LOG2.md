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
class Node:
    def _init_(self, data):
        self.data = data
        self.next = None


class LinkedList:
    def _init_(self):
        self.head = None

    def insert_at_beginning(self, data):
        new_node = Node(data)
        new_node.next = self.head
        self.head = new_node

