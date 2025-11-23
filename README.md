# Operating Systems CPU Scheduling Algorithms Project - 2024

## Academic Context
This project was developed as part of the "Operating Systems" course (2024).

## Team 40 Members

- Yasser Ashraf Mohammed (22010409)
- Wael Ahmed (22010290)
- Ahmed Husein (20225926030)
- Abdurhman Hesham (22010136)
- Moamen Ahmed (22010136)
- Hamza Hussein (22011501)
- Moaz Moustafa (22010263)

## Project Overview

This project implements and visualizes various CPU scheduling algorithms used in operating systems. Each algorithm is implemented with both command-line and GUI interfaces, along with performance metrics calculation and Gantt chart visualization.

## Implemented Algorithms

### 1. First-Come, First-Served (FCFS)
- **Type:** Non-preemptive
- **Implementation:** Yasser Ashraf Mohammed
- **Features:**
  - Process scheduling based on arrival time
  - Gantt chart visualization
  - Performance metrics: Completion Time, Turnaround Time, Waiting Time, Response Time
  - Interactive GUI application with keyboard shortcuts

### 2. Shortest Job First (SJF) - Non-Preemptive
- **Type:** Non-preemptive
- **Implementation:** Wael Ahmed
- **Features:**
  - Processes scheduled by shortest burst time
  - Queue-based implementation
  - Automatic process ID generation
  - Real-time process table updates

### 3. Shortest Remaining Time First (SRTF)
- **Type:** Preemptive
- **Implementation:** Ahmed Husein
- **Features:**
  - Dynamic preemption based on remaining burst time
  - Idle time tracking
  - First execution time recording
  - Comprehensive metrics calculation

### 4. Round Robin
- **Type:** Preemptive
- **Implementation:** Abdurhman Hesham & Moamen Ahmed
- **Features:**
  - Time quantum-based scheduling
  - Fair CPU allocation
  - Response time tracking
  - Average performance metrics

### 5. Priority Scheduling
- **Type:** Both Preemptive and Non-Preemptive
- **Implementation:** Hamza Hussein & Moaz Moustafa
- **Features:**
  - Priority-based process selection
  - Heap-based ready queue implementation
  - Both preemptive and non-preemptive modes
  - Color-coded Gantt charts

## Performance Metrics

All algorithms calculate the following metrics:

- **Completion Time (CT):** Time at which process finishes execution
- **Turnaround Time (TAT):** Total time from arrival to completion (CT - AT)
- **Waiting Time (WT):** Time spent waiting in ready queue (TAT - BT)
- **Response Time (RT):** Time from arrival to first execution
- **Average metrics** for all processes

## GUI Features

### Common Features Across Implementations

- Process input fields (Arrival Time, Burst Time, Process ID)
- Add Process functionality
- Process table display
- Calculate/Run Simulation button
- Reset functionality
- Results display with averages

### Keyboard Shortcuts

- **Enter:** Navigate between fields and add processes
- **Shift+Enter:** Calculate results (where applicable)
- **Backspace:** Delete last process
- **Delete:** Reset all data

## Visualizations

### 1. Gantt Charts
- Visual representation of process execution timeline
- Color-coded process bars
- Time axis with marked intervals
- Process labels

### 2. Bar Plots
- Comparative visualization of Turnaround Time and Waiting Time
- Color-coded metrics
- Process-wise comparison

## Technical Stack

### Libraries Used

- **tkinter:** GUI development
- **matplotlib:** Plotting and visualization
- **numpy:** Numerical operations
- **heapq:** Priority queue implementation
- **tabulate:** Formatted table output

## Installation and Usage

### Prerequisites

```bash
pip install matplotlib numpy tabulate
```

### Running the Programs

Each algorithm can be run independently by executing its respective cell in the notebook or by running the standalone Python script.

### Example Usage

```python
# FCFS Example
processes = [
    Process("P1", 0, 4),
    Process("P2", 1, 3),
    Process("P3", 2, 1),
    Process("P4", 3, 2)
]
scheduled_processes = fcfs_scheduling(processes)
```

## Algorithm Comparisons

### FCFS
- **Advantages:** Simple, easy to implement
- **Disadvantages:** Convoy effect, poor for interactive systems
- **Best for:** Batch systems with long processes

### SJF (Non-Preemptive)
- **Advantages:** Minimizes average waiting time
- **Disadvantages:** Starvation possible, requires burst time knowledge
- **Best for:** Processes with known execution times

### SRTF (Preemptive SJF)
- **Advantages:** Optimal average waiting time
- **Disadvantages:** High context switching overhead
- **Best for:** Time-sharing systems

### Round Robin
- **Advantages:** Fair allocation, no starvation
- **Disadvantages:** Performance depends on time quantum
- **Best for:** Interactive systems

### Priority Scheduling
- **Advantages:** Flexible, supports different process importance
- **Disadvantages:** Potential starvation of low-priority processes
- **Best for:** Real-time systems

## Project Structure

```
Operating Systems Project/
├── OS_FinalProject_Team40.ipynb    # Main notebook
├── OS_FinalProject_Team40.html     # HTML export
├── README.md                        # This file
└── operating system project (1).ipynb
```

## Key Insights

1. **Non-preemptive algorithms** are simpler but may lead to longer waiting times for short processes
2. **Preemptive algorithms** provide better response times but increase context switching overhead
3. **Time quantum selection** in Round Robin significantly impacts performance
4. **Priority scheduling** requires careful design to prevent starvation
5. **FCFS** suffers from convoy effect when long processes arrive first

## Future Enhancements

- Multi-level queue scheduling
- Multi-level feedback queue scheduling
- Real-time scheduling algorithms
- Comparison dashboard for all algorithms
- Process priority aging to prevent starvation
- Dynamic time quantum adjustment for Round Robin

## References

- Operating System Concepts by Silberschatz, Galvin, and Gagne
- Modern Operating Systems by Andrew S. Tanenbaum
- CPU Scheduling research papers and documentation

## License

This project is part of academic coursework for Operating Systems course.