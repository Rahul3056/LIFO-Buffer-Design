### **Day 27: LIFO Buffer Design**

#### **Concept Overview**  
A **LIFO (Last-In First-Out)** buffer is a memory structure where the last element inserted is the first one removed. It functions like a **stack** in software and is used in **backtracking algorithms**, **interrupt handling**, and **expression evaluation**.

#### **Detailed Explanation**  
- **Inputs**  
  - `clk`: Clock  
  - `rst`: Reset  
  - `push`: Push enable  
  - `pop`: Pop enable  
  - `din`: Data input  

- **Outputs**  
  - `dout`: Data output  
  - `full`: Indicates buffer is full  
  - `empty`: Indicates buffer is empty  

- **Internal Register and Pointer**  
  - A stack pointer (`sp`) keeps track of the top of the stack  
  - Push increments the pointer; pop decrements it  

- **Operation**  
  - On `push`, data is written at the current pointer and pointer is incremented  
  - On `pop`, pointer is decremented and data is read  

#### **Applications**  
- Stack memory in CPUs  
- Undo operations in software  
- Nested subroutine calls and return address storage  

#### **Execution Steps**  
1. Define memory array and stack pointer  
2. On reset, initialize stack pointer  
3. On `push`, store data at pointer location and increment it  
4. On `pop`, decrement pointer and read data  
5. Monitor `full` and `empty` flags  

#### **Real-World Example for Practice**  
Create an 8-entry, 8-bit stack and simulate pushing 5 values followed by popping 3 values

#### **Further Enhancements**  
- Add overflow/underflow detection  
- Support dual-port access for faster operation  
- Parameterize depth and width for reuse
