# Designing Urban Parcel Logistics Optimisation System

Final Assignment for **Data Structures and Algorithms (COMP5008)**

## Overview

This project implements a modular urban parcel logistics optimisation system for a fictional company called **CityDrop Logistics**. The system demonstrates how different data structures and algorithms can be used together to support delivery network management, customer record storage, parcel prioritisation, and delivery report sorting.

The project was developed using custom implementations of major abstract data types, including **Graphs, Hash Tables, Heaps, Linked Lists, Queues, and Stacks**. It also includes algorithmic techniques such as **Breadth-First Search, Depth-First Search, Dijkstra’s shortest path algorithm, Quick Sort, and Merge Sort**.

## Project Objectives

The main objectives of this project were to:

- Represent an urban delivery network using a weighted graph.
- Find reachable delivery zones and hop levels using BFS.
- Detect cycles in the delivery network using DFS.
- Calculate shortest delivery paths and travel times using Dijkstra’s algorithm.
- Store and manage customer delivery records using a custom hash table.
- Prioritise parcel delivery requests using a max heap.
- Generate sorted delivery reports using Quick Sort and Merge Sort.
- Compare sorting performance across different input sizes and data orders.

## System Modules

### Module 1: Delivery Network using Graphs

This module represents delivery hubs and routes using a weighted undirected graph.

- Each delivery hub is represented as a vertex.
- Each route between hubs is represented as an edge.
- Edge weights represent travel time between hubs.
- BFS is used to show reachable zones and hop levels.
- DFS is used for cycle detection.
- Dijkstra’s algorithm is used to calculate the shortest delivery path and time.

Supporting structures used:

- Linked List
- Queue
- Stack

### Module 2: Customer Records using Hash Table

This module manages customer records using a custom hash table.

Each customer record includes:

- Customer ID
- Customer name
- Address / delivery zone
- Priority level
- Delivery status

Key features include:

- Insert customer record
- Search customer by ID
- Delete customer record
- Update delivery status
- Auto-adjust priority level based on delivery status
- Collision handling
- Dynamic resizing using load factor
- CSV import and export

### Module 3: Parcel Prioritisation using Max Heap

This module prioritises parcel delivery requests using a max heap.

Each parcel heap node stores:

- Customer ID
- Priority level
- Delivery time
- Delivery status
- Priority score

The heap keeps the highest priority parcel at the top. Priority is calculated using delivery priority and delivery time, allowing urgent and time-sensitive parcels to be handled first.

This module also integrates outputs from:

- Module 1: shortest delivery time from graph
- Module 2: customer record and priority details from hash table

### Module 4: Delivery Report Sorting

This module generates sorted delivery reports using Quick Sort and Merge Sort.

Sorting can be performed by:

- Delivery time
- Delivery zone
- Delivery ID

The module uses external CSV files with different input sizes and data orders to compare sorting performance.

Tested input sizes:

- 100 records
- 500 records
- 1000 records

Tested input orders:

- Nearly sorted
- Random
- Reversed

## Algorithms Implemented

- Breadth-First Search
- Depth-First Search
- Dijkstra’s shortest path algorithm
- Hashing with collision handling
- Max heap insertion and extraction
- Quick Sort
- Merge Sort

## Data Structures Used

- Graph
- Linked List
- Queue
- Stack
- Hash Table
- Hash Entry
- Max Heap
- Heap Node
- NumPy arrays
- Delivery record objects

## Dependencies Used

```python
numpy
csv
time
```
## Dependency Purpose

- **numpy**: Used to create `np.empty` arrays for storing containers of the major data structures.
- **csv**: Used to read input CSV files and write output CSV files.
- **time**: Used to calculate execution time for sorting and performance testing.

## User Instructions

1. Open `Assignmentcode.ipynb`.

2. The file can be run in **Visual Studio Code** with the **Jupyter Notebook extension** installed.

3. Select **Run All** from the top options to run the complete code in a single go.

4. Individual test blocks can also be run separately for testing each module.

5. No user menu was created because it was not required in the assignment. All expected outputs and test methods are already pre-written in the test code.

6. To test different results, only change the relevant values inside the provided test blocks.

7. Do not delete the `Samples` directory or the `output` directory inside the `Samples` directory.

8. Do not amend or delete `customers_record.csv`.

## Repository Contents

### 1. Technical Report

The technical report explains the theory behind the system design. It includes:

- Data structures used
- Module design
- Class diagrams
- Algorithm choices
- Complexity analysis
- Sample outputs
- Limitations and assumptions

### 2. Assignmentcode.ipynb

This is the main code file containing all four modules.

No separate Python files were created because the assignment did not require them, and keeping all modules in one notebook made testing easier.

The notebook includes:

- Graph implementation
- Linked list implementation
- Queue implementation
- Stack implementation
- Hash table implementation
- Heap implementation
- Sorting implementation
- Module testing
- Integration testing

### 3. customers_record.csv

This file contains **75 customer records** used for the demonstration and testing of Module 2.

It is required for:

- Loading customer records into the hash table
- Testing customer search, insert, delete, and update functions
- Demonstrating hash table resizing and collision handling

### 4. Samples Directory

The `Samples` folder contains CSV files used for comparing Quick Sort and Merge Sort performance in Module 4.

Files included:

- `nearly_sorted_100.csv` – 100 records nearly sorted by delivery time
- `nearly_sorted_500.csv` – 500 records nearly sorted by delivery time
- `nearly_sorted_1000.csv` – 1000 records nearly sorted by delivery time
- `random_100.csv` – 100 records randomly sorted by delivery time
- `random_500.csv` – 500 records randomly sorted by delivery time
- `random_1000.csv` – 1000 records randomly sorted by delivery time
- `reversed_100.csv` – 100 records sorted in reverse order by delivery time
- `reversed_500.csv` – 500 records sorted in reverse order by delivery time
- `reversed_1000.csv` – 1000 records sorted in reverse order by delivery time

### 5. Results Files Generated

The code generates the following output files:

- `exported_customers.csv`: Exported customer records from the hash table.
- 18 CSV files generated by Module 4 inside the `Samples/output` directory:
  - 9 result files for Merge Sort
  - 9 result files for Quick Sort

## Complexity Analysis Summary

| Module | Main Operation | Time Complexity |
|---|---|---|
| Graph BFS | Traverse reachable hubs | O(V + E) |
| Graph DFS | Cycle detection | O(V + E) |
| Dijkstra | Shortest path using linked-list scanning | O(V²) |
| Hash Table | Insert, search, delete average case | O(1) |
| Hash Table | Worst case with collisions | O(n) |
| Heap | Insert / extract max | O(log n) |
| Quick Sort | Average case | O(n log n) |
| Quick Sort | Worst case | O(n²) |
| Merge Sort | All cases | O(n log n) |

## Sample Outputs

The project includes sample outputs for:

- Graph adjacency list representation
- Reachable delivery zones from a hub
- BFS traversal with hop levels
- DFS cycle detection
- Dijkstra shortest path and travel time
- Hash table insertion, search, deletion, resizing, and collision handling
- Heap insertion, extraction, and priority update
- Integration testing across graph, hash table, and heap modules
- Sorting performance comparison for 100, 500, and 1000 records

## Skills Demonstrated

This project demonstrates:

- Python programming
- Object-oriented programming
- Data structures and algorithms
- Modular system design
- Graph traversal
- Shortest path calculation
- Hash table implementation
- Heap-based priority queue implementation
- Sorting algorithm implementation
- CSV-based input/output handling
- Algorithm complexity analysis
- Integration testing

## Limitations

- The priority score formula is simplified and does not fully represent a real-world logistics priority model.
- The project avoids built-in Python data structures as part of the assignment requirement, which makes some implementations more complex.
- Dijkstra’s algorithm was implemented using linked-list scanning, resulting in O(V²) complexity.
- The delivery network is simulated and does not use real road network data.
- CSV files are used for demonstration rather than live logistics data.

## Future Improvements

Possible future improvements include:

- Implementing Dijkstra’s algorithm using a priority queue for better efficiency.
- Adding real-world map or road network data.
- Improving the parcel priority score formula.
- Adding a command-line menu or graphical user interface.
- Adding automated unit tests.
- Creating visual route maps for delivery paths.
- Splitting the notebook into separate Python modules for better maintainability.

## Note

This project was developed for academic and portfolio purposes to demonstrate practical understanding of data structures, algorithms, modular programming, and algorithmic performance analysis.
