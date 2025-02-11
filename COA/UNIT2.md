# Computer Organization & Architecture - Unit 2 Detailed Notes

## Basic Computer Organization and Design

In this unit, we delve into the fundamental structure and operational principles of a basic computer system. We'll explore the various components, their interactions, and the design considerations that enable efficient data processing.

### **1. Instruction Codes**

An **instruction code** is a binary representation of operations that a computer's control unit can execute. Each instruction specifies a particular operation and the operands involved.

- **Operation Code (Opcode):** Specifies the operation to be performed (e.g., ADD, SUBTRACT).
- **Operands:** Specify the data or the addresses of the data on which the operation is to be performed.

**Example:**

Consider an instruction code in a 16-bit system:

```
| Opcode (4 bits) | Address (12 bits) |
```

If the opcode `0001` represents the `LOAD` operation, and the address `0010 1100 1010` specifies the memory location, the instruction tells the computer to load data from memory address `2CA` into a register.

### **2. Computer Registers**

Registers are high-speed storage locations within the CPU that temporarily hold data and instructions. They facilitate quick data access and manipulation.

**Common Registers:**

- **Program Counter (PC):** Holds the address of the next instruction to be executed.
- **Instruction Register (IR):** Contains the current instruction being executed.
- **Memory Address Register (MAR):** Holds the address of the memory location to be accessed.
- **Memory Data Register (MDR):** Holds the data to be written to or read from memory.
- **Accumulator (AC):** Used for arithmetic and logic operations.

**Diagram: Basic Computer Registers**

![Basic Computer Registers](https://tse2.mm.bing.net/th?id=OIP.5l8f0e8izMXbqA2r0hZE-wHaFi&pid=Api)

*Note: The diagram illustrates the interconnection of various registers within the CPU.*

### **3. Computer Instructions**

Instructions are commands that dictate the operations the computer performs. They are categorized based on their functions:

- **Data Transfer Instructions:** Move data between registers, memory, and I/O devices.
  - Example: `MOV`, `LOAD`, `STORE`
- **Arithmetic Instructions:** Perform arithmetic operations.
  - Example: `ADD`, `SUBTRACT`, `MULTIPLY`
- **Logical Instructions:** Perform bitwise operations.
  - Example: `AND`, `OR`, `XOR`
- **Control Instructions:** Alter the sequence of execution.
  - Example: `JUMP`, `CALL`, `RETURN`

**Instruction Format:**

An instruction typically consists of:

- **Opcode:** Specifies the operation.
- **Operand(s):** Specify the data or addresses involved.

**Example:**

```
ADD R1, R2  // Adds contents of R2 to R1
```

### **4. Timing and Control**

The **control unit** manages the execution of instructions by generating timing signals that coordinate the activities of the CPU components.

**Control Signals:**

- **Clock Signals:** Synchronize operations.
- **Control Lines:** Direct data flow and operations (e.g., `READ`, `WRITE`).

**Timing Diagram:**

A timing diagram illustrates the sequence of control signals during instruction execution.

**Diagram: Timing Diagram for Instruction Cycle**

![Timing Diagram](https://tse4.mm.bing.net/th?id=OIP.qzQns1QIwXol6UMABng0hgHaEb&pid=Api)

*Note: The diagram shows the sequence of control signals during the fetch, decode, and execute phases.*

### **5. Instruction Cycle**

The **instruction cycle** is the process by which a computer retrieves, decodes, and executes an instruction.

**Phases:**

1. **Fetch:** Retrieve the instruction from memory.
2. **Decode:** Interpret the instruction.
3. **Execute:** Perform the operation.
4. **Store:** Write the result back to memory or a register.

**Diagram: Instruction Cycle**

![Instruction Cycle](https://tse2.mm.bing.net/th?id=OIP.FqeoiHTF6njlfko0YCK-YwHaFj&pid=Api)

*Note: The diagram illustrates the cyclical process of fetching, decoding, executing, and storing instructions.*

### **6. Memory-Reference Instructions**

These instructions involve operations that access memory locations.

**Example:**

```
LOAD R1, 1000  // Load data from memory address 1000 into register R1
```

**Addressing Modes:**

- **Direct Addressing:** The address of the data is specified in the instruction.
- **Indirect Addressing:** The instruction specifies a memory location that contains the address of the data.

**Diagram: Direct vs. Indirect Addressing**

![Addressing Modes](https://tse1.mm.bing.net/th?id=OIP.GzFkGmK_vc-CZ7L79MXlhQAAAA&pid=Api)

*Note: The diagram compares direct and indirect addressing mechanisms.*

### **7. Input-Output and Interrupt**

**Input-Output (I/O):**

I/O operations facilitate communication between the computer and external devices.

- **Programmed I/O:** CPU actively waits and checks for I/O operations.
- **Interrupt-Driven I/O:** Devices signal the CPU when they are ready, allowing the CPU to perform other tasks in the meantime.

**Interrupts:**

Interrupts are signals that alter the CPU's execution flow to address urgent tasks.

**Types:**

- **Hardware Interrupts:** Triggered by hardware devices (e.g., keyboard input).
- **Software Interrupts:** Triggered by software instructions.

**Diagram: Interrupt Process**

![Interrupt Process](https://tse4.mm.bing.net/th?id=OIP.BAhHm-X5mf5Kqg9J-CBLAAHaFj&pid=Api)

*Note: The diagram illustrates how an interrupt alters the normal execution flow.*

### **8. Design of Basic Computer**

Designing a basic computer involves integrating various components to work cohesively.

**Components:**

- **Central Processing Unit (CPU):** Executes instructions.
- **Memory Unit:** Stores data and instructions.
- **Input/Output Devices:** Facilitate user interaction and data exchange.

**Diagram: Basic Computer Design**

![Basic Computer Design](https://tse1.mm.bing.net/th?id=OIP.GzFkGmK_vc-CZ7L79MXlhQAAAA&pid=Api)

*Note: The diagram provides an overview of the basic computer architecture.*

### **Conclusion**

In this unit, we've explored the foundational aspects of computer organization and design, including instruction codes, registers, instruction execution, and the interplay between various components. Understanding these principles is crucial for delving deeper into computer architecture and enhancing system performance.

---

This concludes **Unit 2: Basic Computer Organization and Design**. The next unit will delve into **Central Processing Unit (CPU) Architecture** in detail. 