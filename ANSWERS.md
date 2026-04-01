# Assignment Questions

## Instructions
Answer all 4 questions with detailed explanations. Each answer should be **3-5 sentences minimum** and demonstrate your understanding of the concepts.

---

## Question 1: Thread vs Process

**Question**: Explain the difference between a **thread** and a **process**. Why did we use threads in this assignment instead of creating separate processes?

**Your Answer:**

A process is an independent program in execution that has its own memory space and system resources, while a thread is a smaller unit of execution within a process that shares the same memory. Threads are lighter and faster to create compared to processes, which makes them more efficient for simulations. In this assignment, threads were used because the scheduler is implemented inside a single Java program, and each process is simulated as a thread using new Thread(process). This allows the program to manage multiple tasks without the overhead of creating separate processes. Using processes would require more system resources and inter-process communication, which is unnecessary for this simulation. Therefore, threads are more suitable for implementing Round-Robin scheduling.

---

## Question 2: Ready Queue Behavior

**Question**: In Round-Robin scheduling, what happens when a process doesn't finish within its time quantum? Explain using an example from your program output.

**Your Answer:**

In Round-Robin scheduling, if a process does not finish within its time quantum, it is preempted and moved to the end of the ready queue. This ensures fairness because all processes get equal opportunities to execute. In my output, this behavior is clearly shown when a process completes its quantum but still has remaining time, and then it is re-added to the ready queue. The scheduler then continues executing the next processes in FIFO order. This cycle continues until all processes are completed. This behavior matches the Round-Robin algorithm implemented in the code.

Example from my output:
```
P1 executing quantum [4000ms]
P1 completed quantum 4000ms │ Overall progress: 63%
   Remaining time: 2348ms
P1 yields CPU for context switch
P1 (Priority: 5) added to ready queue
```

**Explanation of example:**
In this example, process P1 executed for the full time quantum of 4000 ms but did not finish because it still had 2348 ms remaining. As a result, it was preempted and returned to the end of the ready queue. The scheduler then moved to the next process in the queue. This demonstrates how Round-Robin scheduling ensures fairness by giving each process a fixed time slice and rotating them in the queue until completion.

---

## Question 3: Thread States

**Question**: A thread can be in different states: **New**, **Runnable**, **Running**, **Waiting**, **Terminated**. Walk through these states for one process (P1) from your simulation.

**Your Answer:**

The thread lifecycle in this simulation can be explained using process P1. First, P1 is in the New state when its thread is created using new Thread(process) in the addProcessToQueue method. It becomes Runnable when it is added to the ready queue and waits for the scheduler to select it. When the scheduler calls currentThread.start(), P1 enters the Running state and begins executing the run() method. The Waiting state occurs when the main thread calls currentThread.join() and waits for the current thread to finish its execution. Finally, P1 reaches the Terminated state when its remaining time becomes zero and the output shows that it finished execution.

1. **New**: When the thread is created using new Thread(process)

2. **Runnable**: When it is added to the ready queue and waiting to be scheduled

3. **Running**: When currentThread.start() is called and execution begins

4. **Waiting**: When currentThread.join() is used and the main thread waits

5. **Terminated**: When execution completes and remaining time becomes zero

---

## Question 4: Real-World Applications

**Question**: Give **TWO** real-world examples where Round-Robin scheduling with threads would be useful. Explain why this scheduling algorithm works well for those scenarios.

**Your Answer:**

### Example 1: Web Server Handling Requests

**Description**: 
A web server receives multiple client requests at the same time, and each request can be handled by a separate thread.

**Why Round-Robin works well here**: 
Round-Robin ensures that each request gets a fair share of CPU time, preventing any single request from blocking others. This improves system responsiveness and allows multiple users to be served efficiently.

### Example 2: Operating System CPU Scheduling

**Description**: 
Operating systems manage multiple processes running simultaneously, such as applications and background services.

**Why Round-Robin works well here**: 
Round-Robin scheduling ensures fairness by giving each process a fixed time quantum. This prevents any process from monopolizing the CPU and ensures smooth performance, especially in interactive systems. In my simulation, processes rotate in the ready queue until they finish, which reflects real OS scheduling behavior.

---

## Summary

**Key concepts I understood through these questions:**
1. The difference between threads and processes in terms of execution and resource usage
2. How Round-Robin scheduling works using time quantum and context switching
3. How threads transition between different states during execution

**Concepts I need to study more:**
1. Thread synchronization and shared resource management
2. Advanced concurrency problems such as race conditions and deadlocks
