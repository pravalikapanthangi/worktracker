# Work Tracker PRO MAX

## Project Overview
Work Tracker PRO MAX is a simple task management system that allows Admins to assign tasks and Members to update their progress. It supports task dependencies, workload tracking, and real-time updates using browser storage.

---

## Features

### Admin Features
- Create and assign tasks
- Set task priority (High, Medium, Low)
- Add dependencies between tasks
- View all tasks and workload distribution
- Detect bottlenecks and blocked tasks
- View charts for task analysis

### Member Features
- View assigned tasks
- Update task progress using slider
- Block/Unblock tasks with reason
- Add notes or updates

---

## Algorithm Explanation

### 1. Dependency Logic
Each task can depend on another task.  
A task can only start when the dependent task reaches a required percentage.

Example:  
Task B starts only after Task A reaches 50%.

---

### 2. Circular Dependency Detection
To avoid infinite loops, the system checks if tasks depend on each other in a cycle.  
If detected, the task is not created.

---

### 3. Smart Workload Calculation
The system calculates how many tasks each user has.  
It helps identify overloaded users and suggests better assignment.

---

### 4. Bottleneck Detection
If a task dependency is not completed, the task is marked as blocked.  
This helps identify delays in workflow.

---

## Setup and Installation

1. Download or clone the project
2. Open the project folder
3. Open `index.html` in any web browser
4. No installation required

---

## Storage Used
The application uses browser `localStorage` to store:
- Users
- Tasks
- Current logged-in user

---

## Test Credentials

**Admin Login:**  
Username: admin  
Password: admin123  

You can also create new users.

---

## Demo Walkthrough
1. Login as Admin  
2. Create tasks and assign them  
3. Add dependencies between tasks  
4. Login as Member  
5. Update task progress  
6. Observe how dependent tasks unlock

---

## Assumptions Made
- The system runs on a single browser using `localStorage`  
- No backend or database is used  
- Task IDs are generated using timestamps

---

## Edge Cases Handled
- Prevents circular dependencies  
- Blocks tasks when dependency is incomplete  
- Handles manual task blocking  
- Detects overloaded users

---

## System Design

### Architecture
- Frontend only (HTML, CSS, JavaScript)  
- No backend server

### Data Model
Each task contains:
- id  
- title  
- description  
- assigned user  
- priority  
- progress  
- blocked status  
- dependency details

---

## Problem Solving Approach
- Broke problem into smaller parts (login, tasks, dependencies)  
- Used functions for modular design  
- Used recursion for dependency cycle detection  
- Stored data using arrays and `localStorage`

---

## Code Quality
- Clean and readable code  
- Modular functions  
- Easy to maintain and extend

---

## User Experience
- Simple and user-friendly interface  
- Interactive progress sliders  
- Clear status indicators (Ready/Blocked)  
- Alerts for important actions

---

## Future Improvements
- Add backend (Node.js)  
- Use database (MongoDB)  
- Improve authentication security  
- Add notifications system

---

## Timeline
Completed within the given 24-hour time limit.

---

## Submission
Repository contains:
- Source code  
- Documentation  
- Setup instructions  
- Test credentials