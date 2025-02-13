Let's delve into **Unit 2: Processes** of our Operating Systems syllabus in detail.

---

# Unit 2: Processes

## 1. Process States

A **process** is a program in execution, encompassing the program code, its current activity, and the associated resources. As a process executes, it transitions through various states:

- **New:** The process is being created.
- **Ready:** The process is prepared to run and is awaiting CPU allocation.
- **Running:** The process is currently executing on the CPU.
- **Waiting (Blocked):** The process is waiting for an event or resource (e.g., I/O completion).
- **Terminated:** The process has completed execution.

These states are often represented in a state diagram, illustrating the transitions between them.

## 2. Process Control Block (PCB)

The **Process Control Block (PCB)** is a data structure maintained by the operating system for each process. It contains essential information, including:

- **Process State:** Current state of the process (e.g., Ready, Running).
- **Process ID (PID):** Unique identifier for the process.
- **Program Counter:** Address of the next instruction to execute.
- **CPU Registers:** Contents of all process-specific registers.
- **Memory Management Information:** Details like page tables or segment tables.
- **Accounting Information:** CPU usage, execution time, etc.
- **I/O Status Information:** List of I/O devices allocated to the process.

The PCB is crucial for context switching, allowing the OS to save and restore process states efficiently.

## 3. Context Switching

**Context switching** is the process by which the operating system saves the state of a currently running process and loads the state of the next process to be executed. This involves:

- Saving the current process's context (its PCB).
- Loading the context of the next scheduled process.

While context switching enables multitasking, it introduces overhead due to the time spent saving and loading process states.

## 4. Threads

A **thread** is the smallest unit of execution within a process. Threads within the same process share resources like memory and file handles but execute independently. There are two primary types:

- **User-Level Threads:** Managed by user-level libraries; the OS is unaware of them.
- **Kernel-Level Threads:** Managed directly by the operating system.

Threads offer benefits such as improved responsiveness and resource sharing but can introduce challenges like synchronization complexities.

## 5. CPU Scheduling

**CPU scheduling** determines the order in which processes access the CPU. There are two main scheduling methods:

### Pre-emptive Scheduling
- **Definition**: A scheduling method where the CPU can be taken away from a process before it completes its execution
- **Characteristics**:
  - Allows interruption of a running process
  - Higher priority processes can interrupt currently running processes
  - Uses priority scheduling and time-sharing concepts
  - Provides better response time and resource utilization
- **Advantages**:
  - Ensures no single process monopolizes the CPU
  - Supports real-time and interactive systems
  - Improves system responsiveness
- **Disadvantages**:
  - Overhead due to frequent context switching
  - More complex implementation
  - Potential for priority inversion

### Non-pre-emptive Scheduling
- **Definition**: A scheduling method where a process runs until it completes or voluntarily yields the CPU
- **Characteristics**:
  - Once a process starts executing, it continues until completion
  - No interruption of running processes
  - Simpler to implement
- **Advantages**:
  - Lower overhead (fewer context switches)
  - Predictable execution
  - Simpler system design
- **Disadvantages**:
  - Potential for process starvation
  - Poor responsiveness
  - Less efficient resource utilization

### Key Differences
| Aspect | Pre-emptive Scheduling | Non-pre-emptive Scheduling |
|--------|------------------------|----------------------------|
| Process Interruption | Allowed | Not allowed |
| CPU Allocation | Can be interrupted mid-execution | Runs to completion |
| Complexity | More complex | Simpler |
| Context Switching | Frequent | Minimal |
| Responsiveness | High | Low |
| Suitable For | Real-time, interactive systems | Batch processing systems |


**CPU scheduling** determines the order in which processes access the CPU. Key concepts include:

- **CPU-I/O Burst Cycle:** Processes alternate between CPU execution and I/O operations.
- **CPU Scheduler:** Selects processes from the ready queue for execution.
- **Dispatcher:** Handles the actual context switching to the selected process.

Common scheduling algorithms:

- **First-Come, First-Served (FCFS):** Processes are scheduled in the order they arrive.
- **Shortest Job Next (SJN):** Selects the process with the smallest execution time.
- **Round Robin (RR):** Each process is assigned a fixed time slice in a cyclic order.
- **Priority Scheduling:** Processes are scheduled based on priority levels.
- **Real-Time Scheduling:** Ensures processes meet specific timing constraints, using algorithms like Rate Monotonic (RM) and Earliest Deadline First (EDF).


Each algorithm has its advantages and trade-offs concerning factors like throughput, turnaround time, and fairness.
