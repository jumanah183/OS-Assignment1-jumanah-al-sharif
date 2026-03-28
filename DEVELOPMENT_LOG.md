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

### Entry 1 - [Date and Time]
**What I did**:  Initial project setup and code review.

**Details**: Understanding the base scheduler code and identifying where to add new features.

**Challenges**: Getting familiar with the existing logic of the process simulation.

**Solution**: Drawing a flowchart of the process execution to visualize the flow.

**Time spent**: 2 hours.

---

### Entry 2 - [Date and Time]
**What I did**: Implementing Feature 1 (Priority System).

**Details**: Added a random priority generator (1-5) and updated the Process class.

**Challenges**: The priority wasn't being correctly assigned to each process in the loop.
**Solution**:  Verified the random seed and ensured the priority parameter is passed correctly to the constructor.

**Time spent**: 3.5 hours

---

### Entry 3 - [Date and Time]
**What I did**:  Implementing Feature 2 (Context Switch Tracking).

**Details**:  Added a counter to track every time the CPU switches between processes.

**Challenges**:  Deciding the exact point where the switch occurs to increment the counter correctly.

**Solution**:  Placed the counter increment inside the scheduler loop whenever a new process is loaded.

**Time spent**: 2.5 hours

---

### Entry 4 - [Date and Time]
**What I did**: Integrating Feature 3 (Waiting Time Summary Table).

**Details**:  Added the displayWaitingTimeSummary method to the main simulation flow to show each process's details.

**Challenges**:  Ensuring that the waiting time for each process is captured correctly throughout the scheduling cycles.

**Solution**: Used a list to store the final state of each process and then passed it to the summary method for display.

**Time spent**:  2 hours.

---

### Entry 5 - [Date and Time]
**What I did**: Developing and merging the custom features into the main project.

**Details**:  I wrote the code for Priority and Context Switches in a separate test script first to ensure they worked, then I moved them into the main class.

**Challenges**: Some variables didn't match the main class structure during the move.

**Solution**: Renamed and adjusted the variables to fit the main simulation logic perfectly.

**Time spent**:  2.5 hours.

---

### Entry 6 - [Optional - Date and Time]
**What I did**: 

**Details**: 

**Challenges**: 

**Solution**: 

**Time spent**: 

---

## Summary

**Total time spent on assignment**: [X hours]

**Most challenging part**: 

**Most interesting learning**: 

**What I would do differently next time**: 
