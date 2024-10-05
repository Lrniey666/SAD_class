# Project Task Flowchart and Gantt Chart

## 1. PERT/CPM Diagram
Below is the PERT/CPM diagram of the project, showing the dependencies between tasks:

```mermaid
graph TD
    A[Research Plan 1 day] --> B[Task Assignment 4 days]
    A --> C[Hardware Acquisition 17 days]
    B --> D[Program Development 70 days]
    C --> E[Hardware Installation 10 days]
    D --> F[Program Testing 30 days]
    E --> G[User Manual Writing 25 days]
    E --> H[File Conversion 20 days]
    F --> I[System Testing 25 days]
    G --> J[User Training 20 days]
    H --> J
    I --> K[User Testing 25 days]
    J --> K
gantt
    title Project Gantt Chart
    dateFormat  YYYY-MM-DD
    section Research and Resource Acquisition
    Research Plan            :done,  task1, 2024-10-01, 1d
    Task Assignment          :active, task2, after task1, 4d
    Hardware Acquisition     :active, task3, after task1, 17d
    section Program Development and Testing
    Program Development      :        task4, after task2, 70d
    Program Testing          :        task6, after task4, 30d
    section Installation and System Integration
    Hardware Installation    :        task5, after task3, 10d
    User Manual Writing      :        task7, after task5, 25d
    File Conversion          :        task8, after task5, 20d
    section System Testing and Acceptance
    System Testing           :        task9, after task6, 25d
    User Training            :        task10, after task7, 20d
    User Training            :        task10, after task8, 20d
    User Testing             :        task11, after task9, 25d
    User Testing             :        task11, after task10, 25d
