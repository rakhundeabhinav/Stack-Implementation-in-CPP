
## 📦 Queue and Stack in C++

### 🎯 Aim  
To implement **Queue** and **Stack** operations in C++ using arrays, and to understand their differences in terms of memory allocation, processing order, and operational efficiency.

---

### 📚 Theory  

#### 🔁 Queue  
A **Queue** is a linear data structure that follows the **FIFO (First In, First Out)** principle.  
- **Front** → points to the first element  
- **Rear** → points to the last element  

**Key Characteristics**:  
- Insertion at rear, deletion from front  
- FIFO order  
- Overflow when full, underflow when empty  

#### 🔃 Stack  
A **Stack** is a linear data structure that follows the **LIFO (Last In, First Out)** principle.  
- **Top** → points to the most recently inserted element  

**Key Characteristics**:  
- Insertion and deletion at top only  
- LIFO order  
- Overflow when full, underflow when empty  

---

### 📋 Algorithms  

#### ✅ Queue (Array-Based)

1. Initialize `front = -1`, `rear = -1`, and define `arr[SIZE]`  
2. Display menu:
   - Enqueue, Dequeue, Display, Peek, Check Empty, Check Full, Size, Clear, Exit  
3. Loop until Exit:
   - **Enqueue**:  
     - If `rear == SIZE - 1` → Overflow  
     - If `front == -1` → set `front = 0`  
     - Increment `rear`, insert at `arr[rear]`  
   - **Dequeue**:  
     - If `front == -1` or `front > rear` → Underflow  
     - Print `arr[front]`, increment `front`  
     - If `front > rear` → reset both to `-1`  
   - **Display**:  
     - Traverse from `front` to `rear`  
   - **Peek**:  
     - Show `arr[front]`  
   - **Check Empty**:  
     - If `front == -1` or `front > rear`  
   - **Check Full**:  
     - If `rear == SIZE - 1`  
   - **Size**:  
     - `rear - front + 1`  
   - **Clear**:  
     - Reset `front = rear = -1`  
   - **Exit**:  
     - Terminate program  

#### ✅ Stack (Array-Based)

1. Initialize `top = -1` and define `arr[MAX]`  
2. Display menu:
   - Push, Pop, Display, Exit  
3. Loop until Exit:
   - **Push**:  
     - If `top == MAX - 1` → Overflow  
     - Increment `top`, insert at `arr[top]`  
   - **Pop**:  
     - If `top == -1` → Underflow  
     - Print `arr[top]`, decrement `top`  
   - **Display**:  
     - Traverse from `top` to `0`  
   - **Exit**:  
     - Terminate program  

---

### 🚀 Applications  

#### Queue  
- CPU scheduling (Round Robin, FCFS)  
- Disk scheduling  
- Data buffering (IO buffers, print queues)  
- BFS in graphs  
- Order processing systems  

#### Stack  
- Expression evaluation (postfix, prefix)  
- Function call management (recursion)  
- Undo/Redo in editors  
- Backtracking algorithms  
- Browser history navigation  
- Parsing and compilation  

---

### 🧠 Conclusion  
- **Queue** follows FIFO, ideal for scheduling and buffering tasks.  
- **Stack** follows LIFO, suitable for recursion, parsing, and backtracking.  
Both are foundational data structures in DSA, enabling efficient memory management, expression evaluation, and graph traversal.
