# Development Log

## Instructions
Document your development process as you work on the assignment. Add entries showing:
- What you worked on
- Problems you encountered
- How you solved them
- Time spent

**Requirements**: Minimum 5 entries showing progression over time.

---

## Example Entry Format:

### Entry 1 - [April 1, 2026, 2:30 PM]
**What I did**: Forked the repository and set up my student ID

**Details**: 
- Created GitHub account with university email
- Forked the starter repository
- Changed student ID on line 92 to my actual ID (441234567)
- Compiled and ran the program successfully

**Challenges**: Had to install JDK first because javac wasn't recognized

**Solution**: Downloaded JDK 17 from Oracle website and set PATH variable

**Time spent**: 30 minutes

---

## Your Development Log:

### Entry 1 - [March 30, 2026, 7:48 PM]
**What I did**: Set up the project and configured my student ID 

**Details**: 
- Forked the repository from GitHub
- Opened the project in VS Code
- Updated the student ID in the code
- Ran the program successfully for the first time

**Challenges**: Initially, I had trouble running the program because I was using an outdated version of the JDK, which caused errors when compiling and executing the code.

**Solution**: I installed the latest version of the JDK (JDK 26) and updated my VS Code Java extensions. After configuring the correct JDK path, the program ran successfully without errors.

**Time spent**: 40 minutes

---

### Entry 2 - [March 31, 2026, 12:45 AM]
**What I did**: Implemented Feature 1 (Process Priority) 

**Details**: 
- Added a priority field to the Process class
- Modified the constructor to accept priority
- Generated random priority values between 1 and 5
- Displayed priority when processes enter the ready queue

**Challenges**: I initially forgot to pass the priority value correctly to the constructor 

**Solution**: I updated the constructor and ensured the priority value is passed during process creation

**Time spent**: 2 hours and 30 minutes

---

### Entry 3 - [March 31, 2026, 3:56 AM]
**What I did**: Implemented Feature 2 (Context Switch Tracking)

**Details**: 
- Added a static variable to count context switches
- Incremented the counter before each thread execution
- Printed the total number of context switches at the end

**Challenges**: I was unsure where to increment the counter for accurate results

**Solution**: I placed the counter increment before currentThread.start() to correctly count each execution

**Time spent**: 2 hours 

---

### Entry 4 - [March 31, 2026, 5:52 PM]
**What I did**: Started implementing Feature 3 (Waiting Time)

**Details**: 
- Added variables for creation time, enqueue time, and total waiting time
- Implemented methods to track waiting time
- Added logic to update enqueue time when processes re-enter the queue

**Challenges**: The waiting time calculation was incorrect at first 

**Solution**: I realized the calculation must be done before execution, not after, and adjusted the code accordingly

**Time spent**: 1 hour and 30 minutes

---

### Entry 5 - [April 1, 2026, 5:15 PM]
**What I did**: Final testing and validation

**Details**: 
- Ran the full simulation
- Verified all features (priority, context switch, waiting time)
- Checked output formatting and correctness

**Challenges**: Ensuring all features work together without breaking the original logic

**Solution**: Tested each feature step by step and confirmed integration

**Time spent**: 45 minutes

---

## Summary

**Total time spent on assignment**: 7 hours and 25 minutes

**Most challenging part**: 
Correctly implementing the waiting time computation was the most difficult element. Initially, I placed the calculation after the process execution, which led to inaccurate results. Finding the right place in the code without interfering with the Round-Robin scheduling mechanism was also challenging. Debugging was also necessary to correct syntax errors such as misplaced brackets.

**Most interesting learning**: 
The most fascinating aspect was realizing how Round-Robin scheduling operates. I was able to make the connection between theory and practical application by seeing how processes enter and exit the ready queue and how context switching takes place. I also gained a better understanding of how scheduling impacts process performance by keeping track of waiting times.

**What I would do differently next time**: 
Next time, I would not wait until the very end to begin testing and implementing each feature. In order to prevent several problems at once, I would additionally test every feature as soon as it is implemented. Before writing any code, I would also take additional time to consider where to add new logic.
