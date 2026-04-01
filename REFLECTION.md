# Reflection Questions

## Instructions
Answer the following questions about your learning experience. Each answer should be **at least 5-7 sentences** and show your understanding.

---

## Question 1: What did you learn about multithreading?

**Your Answer:**

This assignment helped me understand how multithreading allows multiple tasks to run efficiently within a single process. I learned how to create and execute threads in Java using new Thread() and the start() method. I also understood the thread lifecycle, including the states New, Runnable, Running, Waiting, and Terminated. By implementing the Round-Robin scheduler, I saw how CPU time is shared between threads using a fixed time quantum. I also learned how methods like join() and sleep() affect execution and coordination between threads. This assignment helped me connect theoretical concepts from operating systems with practical implementation. Overall, I now have a better understanding of how scheduling works in a multi-threaded environment.

---

## Question 2: What was the most challenging part of this assignment?

**Your Answer:**

The most challenging part of this assignment was implementing the waiting time calculation correctly. At first, I placed the calculation after the process execution, which resulted in incorrect waiting time values. It was difficult to determine the correct location in the code to update the waiting time without affecting the Round-Robin scheduling logic. I also faced syntax errors caused by misplaced brackets, which required careful debugging. Understanding how processes move in and out of the ready queue required close attention to the program flow. In addition, I had to make sure that each feature worked without breaking the original functionality. These challenges required multiple attempts and testing.

---

## Question 3: How did you overcome the challenges you faced?

**Your Answer:**

I overcame these challenges by carefully analyzing the code and understanding how the scheduler loop works step by step. I ran the program several times and compared the output with the expected behavior to identify errors. When I noticed incorrect waiting time values, I traced the logic and realized that the calculation should be done before execution. I used debugging techniques to fix syntax errors and ensure the code structure was correct. I also tested each feature separately before combining them together. This approach helped me avoid breaking the original functionality. Breaking the problem into smaller parts made it easier to solve each issue effectively.

---

## Question 4: How can you apply multithreading concepts in real-world applications?

**Your Answer:**

Multithreading is widely used in real-world applications such as web browsers, where multiple tabs run at the same time. It is also used in games, where graphics rendering, sound processing, and user input run in parallel. In server applications, multithreading allows handling multiple client requests simultaneously. Mobile applications also use threads to perform background tasks without freezing the user interface. In this assignment, I simulated how a CPU scheduler manages multiple processes, which is similar to how operating systems handle real tasks. This shows how multithreading improves system performance and responsiveness. These concepts are essential for building efficient and scalable software systems.

---

## Additional Reflections (Optional)

### What would you like to learn more about?

[Any topics related to threading, concurrency, or operating systems that you're curious about?]

---

### How confident do you feel about multithreading concepts now?

Intermediate

After completing this assignment, I feel more confident about the basic concepts of multithreading. I understand how threads are created, scheduled, and executed in a program. I also gained experience in implementing scheduling logic and analyzing program behavior. However, I still need more practice with advanced topics such as synchronization and concurrency control. I can apply the basic concepts, but I need deeper understanding for more complex scenarios. Overall, my confidence has improved significantly.

---

### Feedback on the assignment

This assignment was very helpful in connecting theory with practical implementation. It helped me understand how CPU scheduling works in a real program. The tasks were challenging but achievable, which made the learning process effective. I especially liked how each feature built on the previous one. It also improved my debugging and problem-solving skills. The assignment provided a good balance between theory and practice. Overall, it was a valuable learning experience.
