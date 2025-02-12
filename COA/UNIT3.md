# Computer Organization & Architecture - Unit 3 Detailed Notes

## Central Processing Unit (CPU)

The Central Processing Unit (CPU) is the primary component of a computer that performs most of the processing inside a computer. It executes instructions from programs through a sequence of operations, including fetching, decoding, and executing instructions.

### **1. Introduction to CPU**

The CPU is often referred to as the "brain" of the computer. It consists of two main units:

- **Arithmetic Logic Unit (ALU):** Performs arithmetic and logical operations.
- **Control Unit (CU):** Directs operations within the processor by interpreting instructions and initiating appropriate actions.

![CPU Block Diagram](https://tse1.mm.bing.net/th?id=OIP.5l8f0e8izMXbqA2r0hZE-wHaFi&pid=Api)

### **2. Instruction Formats**

An instruction format defines the layout of bits in an instruction, specifying the operation to be performed and the operands involved. The common instruction formats include:

- **Zero-Address Instructions:** Implicitly use a stack for operations.
- **One-Address Instructions:** Use a single address field; the other operand is implied (e.g., accumulator).
- **Two-Address Instructions:** Specify two address fields for operands.
- **Three-Address Instructions:** Include three address fields, typically for complex operations.

#### **Example of Instruction Formats:**

1. **Zero-Address (Stack-Based):**
   ```
   PUSH A
   PUSH B
   ADD
   POP C
   ```
   Here, `A` and `B` are pushed onto the stack, added, and the result is popped into `C`.

2. **One-Address:**
   ```
   LOAD A
   ADD B
   STORE C
   ```
   This uses an accumulator to perform operations.

3. **Two-Address:**
   ```
   MOV A, B
   ADD A, C
   ```
   The result is stored in one of the operand locations.

4. **Three-Address:**
   ```
   ADD A, B, C
   ```
   This means `A = B + C`.

### **3. Addressing Modes**

Addressing modes determine how the operand of an instruction is chosen. Common addressing modes include:

- **Immediate Addressing:** Operand is part of the instruction.
- **Direct Addressing:** Address field contains the effective address of the operand.
- **Indirect Addressing:** Address field points to a memory location that contains the effective address.
- **Register Addressing:** Operand is in a register.
- **Register Indirect Addressing:** Register contains the address of the operand.
- **Indexed Addressing:** Combines a base address with an index.
- **Base-Register Addressing:** Uses a base register to hold the starting address.

#### **Diagram: Addressing Modes**

![Addressing Modes](https://tse4.mm.bing.net/th?id=OIP.qzQns1QIwXol6UMABng0hgHaEb&pid=Api)

### **4. Data Transfer and Manipulation**

Data transfer instructions move data between registers, memory, and I/O devices. Data manipulation instructions perform operations on data.

#### **Data Transfer Instructions:**

- **MOV:** Transfer data from source to destination.
- **LOAD:** Load data from memory to a register.
- **STORE:** Store data from a register to memory.

#### **Data Manipulation Instructions:**

- **Arithmetic Operations:** ADD, SUB, MUL, DIV.
- **Logical Operations:** AND, OR, XOR, NOT.
- **Shift Operations:** SHL (shift left), SHR (shift right).

### **5. Program Control**

Program control instructions alter the sequence of execution. They include:

- **Branch Instructions:** Conditional and unconditional jumps to other parts of the program.
- **Subroutine Call and Return:** Transfer control to a subroutine and return to the main program.
- **Loop Control:** Instructions that manage looping constructs.

#### **Example:**

```
CMP A, B
JNE LABEL
```

This compares `A` and `B` and jumps to `LABEL` if they are not equal.

### **6. Reduced Instruction Set Computer (RISC)**

RISC is a CPU design philosophy that focuses on a small, highly optimized set of instructions.

#### **Characteristics of RISC:**

- **Simple Instructions:** Each instruction performs a simple operation.
- **Uniform Instruction Format:** Fixed-length instructions for simplicity.
- **Load/Store Architecture:** Separate instructions for memory access and ALU operations.
- **Large Number of Registers:** To minimize memory access.

#### **Diagram: RISC Architecture**

![RISC Architecture](https://tse2.mm.bing.net/th?id=OIP.FqeoiHTF6njlfko0YCK-YwHaFj&pid=Api)

### **7. Complex Instruction Set Computer (CISC)**

CISC is a CPU design philosophy that emphasizes a rich set of instructions, including complex operations.

#### **Characteristics of CISC:**

- **Complex Instructions:** Single instructions can perform multiple operations.
- **Variable Instruction Length:** Instructions vary in size.
- **Fewer Registers:** Relies more on memory operations.
- **Microprogrammed Control Unit:** Uses microcode to implement complex instructions.

#### **Diagram: CISC Architecture**

![CISC Architecture](https://tse4.mm.bing.net/th?id=OIP.BAhHm-X5mf5Kqg9J-CBLAAHaFj&pid=Api)

### **8. Comparison of RISC and CISC**

| Feature               | RISC                                  | CISC                                  |
|-----------------------|---------------------------------------|---------------------------------------|
| Instruction Complexity| Simple, single-cycle instructions     | Complex, multi-cycle instructions     |
| Instruction Length    | Fixed                                 | Variable                              |
| Addressing Modes      | Few                                   | Many                                  |
| Registers             | Many                                  | Few                                   |
| Memory Access         | Load/store architecture               | Memory-to-memory operations           |
| Control Unit          | Hardwired                             | Microprogrammed                       |

### **Conclusion**

- The CPU is central to computer operations, executing instructions through various formats and addressing modes.
- Data transfer, manipulation, and program control instructions enable complex computing tasks.
- RISC and CISC represent two different philosophies in CPU design, each with its advantages and trade-offs.

---

This concludes **Unit 3: Central Processing Unit**. The next unit will delve into **Memory Organization** in detail. 