# CPU Scheduling Algorithms – Operating Systems Simulation Suite

A comparative simulation and visualization suite for classical **CPU scheduling algorithms**, focusing on execution behavior, performance metrics, and scheduling trade-offs.

**Context:** Operating Systems Course Project (2024)

---

## Project Overview

This project implements and analyzes the most widely used **CPU scheduling algorithms** taught in operating systems.  
Rather than only implementing formulas, it focuses on **behavioral comparison**, **metric evaluation**, and **visual interpretation** of scheduling decisions.

The system provides:
- Multiple scheduling strategies (preemptive & non-preemptive)
- Quantitative performance metrics
- Gantt chart visualizations
- GUI-based interaction for simulation

---

## Implemented Scheduling Algorithms

### 1. First-Come, First-Served (FCFS)
- Non-preemptive
- Schedules processes strictly by arrival order
- Demonstrates convoy effect and fairness limitations

---

### 2. Shortest Job First (SJF – Non-Preemptive)
- Selects process with minimum burst time
- Minimizes average waiting time
- Illustrates starvation risk

---

### 3. Shortest Remaining Time First (SRTF)
- Preemptive version of SJF
- Dynamically switches based on remaining execution time
- Improves response time at the cost of context switching

---

### 4. Round Robin (RR)
- Time-sliced, preemptive scheduling
- Ensures fairness and responsiveness
- Performance highly dependent on time quantum selection

---

### 5. Priority Scheduling
- Supports both preemptive and non-preemptive modes
- Schedules based on priority levels
- Highlights starvation and priority inversion issues

---

## Performance Metrics

All algorithms are evaluated using standard OS metrics:

- **Completion Time (CT)**
- **Turnaround Time (TAT)**
- **Waiting Time (WT)**
- **Response Time (RT)**
- **Average metrics** across processes

These metrics enable **quantitative comparison** between scheduling strategies.

---

## Visualization & Interaction

The project emphasizes **visual understanding** of scheduling behavior:

- Gantt charts for execution timelines
- Color-coded process execution
- Comparative bar plots for waiting and turnaround times
- GUI-based simulation using keyboard shortcuts

This helps bridge theory with observable runtime behavior.

---

## Technical Highlights

- Python-based simulation
- GUI implementation using `tkinter`
- Visualization with `matplotlib`
- Priority queues via `heapq`
- Modular algorithm implementations
- Independent execution per algorithm

---

## Engineering Focus

This project demonstrates:
- Understanding of preemptive vs non-preemptive scheduling
- Trade-offs between fairness, throughput, and response time
- Practical implications of scheduling design
- Clear separation between algorithm logic and visualization

It is designed as a **learning and comparison tool**, not just a code exercise.

**Status:** Completed academic project  
**Scope:** Operating systems scheduling analysis & simulation
