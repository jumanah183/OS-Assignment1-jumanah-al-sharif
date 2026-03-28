# Assignment Questions

## Instructions
Answer all 4 questions with detailed explanations. Each answer should be **3-5 sentences minimum** and demonstrate your understanding of the concepts.

---

## Question 1: Thread vs Process

**Question**: Explain the difference between a **thread** and a **process**. Why did we use threads in this assignment instead of creating separate processes?

**Your Answer:**

[process is an independent program execution with its own memory space, while a thread is a smaller unit of execution within a process that shares the same memory. In this assignment, we used threads because they are 'lightweight' and share the same resources (like processQueue and processMap), which makes communication between them faster and reduces the overhead compared to creating separate processes]

---

## Question 2: Ready Queue Behavior

**Question**: In Round-Robin scheduling, what happens when a process doesn't finish within its time quantum? Explain using an example from your program output.

**Your Answer:**

["In Round-Robin scheduling, if a process doesn't finish within its timeQuantum, it's sent back to the queue. In my SchedulerSimulation.java (Line 267), I use addProcessToQueue to manage this flow]

Example from my output:
```
[PaLooking at the terminal, process P1 has a Burst Time of 2408ms. Since my timeQuantum is set between 2000ms and 5000ms (Line 216), P1 might not finish in one turn. The table shows its Waiting Time is 31ms, which proves it was placed in the Ready Queue and had to wait for its turn to execute again."ste a relevant snippet from your program output here showing a process being re-queued]
```

**Explanation of example:**
[Explain what's happening in the output snippet you pasted]

---

## Question 3: Thread States

**Question**: A thread can be in different states: **New**, **Runnable**, **Running**, **Waiting**, **Terminated**. Walk through these states for one process (P1) from your simulation.

**Your Answer:**

[I implemented a priority system where each process gets a random priority between 1 and 5 (Line 260). Higher numbers mean higher importance. In my summary table, P7 has a Priority of 5, while P8 has a Priority of 2. This allows the scheduler to favor critical tasks, directly affecting their execution order and waiting times]

1. **New**: [When P1 is created as an object: new Process("P1", ...) (Line 264).]

2. **Runnable**: [When P1 is added to the processQueue (Line 267) and waits for its turn.]

3. **Running**: [When the scheduler starts the thread and it executes the run() method (Line 62)]

4. **Waiting**: [When P1 calls Thread.sleep() (Line 78) to simulate processing time.]

5. **Terminated**: [When the process finishes its work and its thread stops.]

---

## Question 4: Real-World Applications

**Question**: Give **TWO** real-world examples where Round-Robin scheduling with threads would be useful. Explain why this scheduling algorithm works well for those scenarios.

**Your Answer:**

### Example 1: [Web Server Handling Requests]

**Description**: 
[web server (like Apache or Nginx) uses Round-Robin to handle multiple incoming user requests. Each user request is assigned to a thread]

**Why Round-Robin works well here**: 
[It ensures fairness. No single user can 'hog' the server resources for too long. By giving each request a small time slice, the server stays responsive to all users simultaneously]

### Example 2: [Operating System Task Manager]

**Description**: 
[Modern Operating Systems (Windows or macOS) use Round-Robin to manage multiple background threads like system updates, antivirus scans, and UI rendering]

**Why Round-Robin works well here**: 
[It provides high predictability and responsiveness. It prevents background tasks (like a scan) from freezing the entire computer, allowing the user to continue interacting with the screen smoothly.]

---

## Summary

**Key concepts I understood through these questions:**
1. Concurrency vs Parallelism: I understood how threads allow multiple tasks to share the same CPU core by switching quickly between them (Concurrency).
2. Scheduling Overhead: I learned that features like "Context Switching" are necessary for multitasking but come with a performance cost that needs to be balanced.
3. Resource Sharing: I understood how threads within the same process can communicate and share data structures like the processQueue much faster than independent processes.

**Concepts I need to study more:**
Deadlock Prevention: I want to learn more about how to prevent multiple threads from waiting for each other forever in more complex systems.
• Synchronization Objects: I am curious about using "Semaphores" or "Locks" to ensure that shared data doesn't get corrupted when many threads access it at once.
1. 
2. 
