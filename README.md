# stack.array-cpp
This program demonstrates the implementation and operation of a **Stack** data structure using a static array in C++.

***

### **Aim**

To implement a **Stack** data structure using a class and a fixed-size array, demonstrating the core operations of **push**, **pop**, **peek**, and **display**.

***

### **Theory**

A **Stack** is a linear data structure that follows the **LIFO** (Last-In, First-Out) principle, meaning the element inserted last is the one removed first.

* **Pointer:** The stack uses a single pointer, **`top`**, which keeps track of the index of the topmost element in the array. The stack is initialized with `top = -1`, indicating it's empty.
* **Operations:**
    * **`push` (Insertion):** Elements are added to the stack by incrementing `top` and inserting the value into `ar[top]`.
        * **Overflow:** Occurs if `top` reaches the maximum size limit (`size - 1`).
    * **`pop` (Deletion):** The element at the `top` is retrieved and removed by decrementing `top`.
        * **Underflow:** Occurs if the stack is empty (`top == -1`).
    * **`peak` (Access):** Returns the value of the top element without removing it.
    * **`disp` (Display):** Prints all elements currently in the stack from the bottom up.

***

### **Algorithm**

1.  **Define Constants and Class:**
    a.  Define constants `size` (as 5) for capacity and `ERROR` (as -9999) for error returns.
    b.  Define a class `Stack` with a private array `ar[size]` and a private integer `top` initialized to $-1$ in the constructor.
    c.  Declare public methods: `push`, `pop`, `peak`, and `disp`.
2.  **`push(int num)` Method:** Check for **Overflow**; if not full, increment `top` and assign `num` to `ar[top]`.
3.  **`pop()` Method:** Check for **Underflow**; if not empty, retrieve `ar[top]`, decrement `top`, and return the value.
4.  **`peak()` Method:** Check for **Underflow**; if not empty, return the value of `ar[top]` without modifying `top`.
5.  **`disp()` Method:** Check for **Underflow**; if not empty, iterate through the array from index $0$ up to `top` and print the elements.
6.  **In `main`:**
    a.  Create a `Stack` object `s1`.
    b.  Push the values $7, 10, 4$ onto the stack.
    c.  Call `pop()` to remove and print the top element.
    d.  Call `peak()` to retrieve and print the new top element.
    e.  Call `disp()` to print the remaining elements of the stack.

***

### **Conclusion**

This experiment successfully implemented the **Stack** data structure following the **LIFO** principle using an array. It demonstrated the practical application of `top` for managing insertions (`push`) and deletions (`pop`), along with essential error handling for **Overflow** and **Underflow** conditions.
