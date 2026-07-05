# Urban Parcel Logistics System using Data Structures and Algorithms

## Overview

This project implements a modular parcel logistics system for a fictional company, **CityDrop Logistics**, using custom data structures and algorithms. The system was designed to optimise different parts of an urban delivery network, including delivery zone mapping, customer record management, parcel prioritisation, and end-of-day delivery report sorting.

The project was completed as part of the COMP5008 Data Structures and Algorithms final assignment.

## Project Objective

The main objective of this project was to design and implement a logistics system using core abstract data types and algorithms without relying heavily on built-in data structures.

The system includes four main modules:

- Delivery network representation using graphs
- Customer information storage using a hash table
- Parcel prioritisation using a max heap
- Delivery report sorting using quick sort and merge sort

## System Modules

### Module 1: Delivery Network Graph

The delivery network was represented using a weighted undirected graph.

In this module:

- Each delivery hub or zone is represented as a graph vertex.
- Connections between hubs are represented as weighted edges.
- Edge weights represent the travel time between delivery zones.
- An adjacency list structure was used to store graph connections.

Algorithms implemented:

- Breadth-First Search for reachable zones and hop-level traversal
- Depth-First Search for cycle detection
- Dijkstra’s algorithm for shortest path and delivery time calculation

Supporting data structures:

- Custom linked list
- Custom queue
- Custom stack

## Module 2: Customer Hash Table

A custom hash table was implemented to store and manage customer delivery records.

Each customer record includes:

- Customer ID
- Customer name
- Address / delivery zone
- Priority level
- Delivery status

Key features:

- Insert customer record
- Search customer by ID
- Delete customer record
- Update delivery status
- Auto-adjust priority level based on delivery status
- Collision handling using probing
- Dynamic resizing based on load factor
- CSV import and export support

A custom hash function using shift, add, and XOR logic was used to distribute string-based customer IDs across the table.

## Module 3: Parcel Priority Queue using Max Heap

A max heap was implemented to manage parcel delivery priority.

Each heap node stores:

- Customer ID
- Priority level
- Delivery time
- Delivery status
- Calculated priority score

The heap ensures that the parcel with the highest priority score remains at the top.

Key features:

- Insert parcel request
- Update parcel request
- Extract highest priority parcel
- Heapify up and heapify down
- Dynamic heap resizing
- Integration with customer hash table and delivery graph

This module connects the graph and hash table modules by using customer ID, delivery zone, priority level, and shortest delivery time.

## Module 4: Delivery Report Sorting

Sorting algorithms were implemented to generate end-of-day delivery reports.

Algorithms implemented:

- Quick Sort
- Merge Sort

Sorting can be performed by:

- Delivery time
- Delivery zone
- Delivery ID

The module also supports reading delivery records from CSV files and exporting sorted results into new CSV files.

## Algorithms Used

This project includes the implementation of:

- Breadth-First Search
- Depth-First Search
- Dijkstra’s shortest path algorithm
- Hashing with collision handling
- Max heap insertion and extraction
- Quick Sort
- Merge Sort

## Data Structures Used

The project uses the following custom data structures:

- Graph
- Linked List
- Queue
- Stack
- Hash Table
- Hash Entry
- Max Heap
- Heap Node
- NumPy arrays for internal storage
- Delivery record objects

## Integration Design

The modules were designed to work independently and as part of an integrated logistics system.

The integration works as follows:

1. The graph module calculates delivery times between zones.
2. The hash table stores customer records and delivery zones.
3. The heap module combines customer priority and delivery time to prioritise parcels.
4. The sorting module generates final delivery reports.

This structure demonstrates how multiple data structures can work together in a real-world logistics scenario.

## Complexity Analysis

The project includes algorithm complexity analysis for all major operations.

Examples:

- Graph BFS: O(V + E)
- Graph DFS: O(V + E)
- Dijkstra’s algorithm using linked-list scanning: O(V²)
- Hash table insert/search/delete average case: O(1)
- Hash table worst case with collisions: O(n)
- Heap insert and extract max: O(log n)
- Quick Sort average case: O(n log n)
- Quick Sort worst case: O(n²)
- Merge Sort: O(n log n)

## Sample Outputs

The project includes sample outputs for:

- Graph adjacency list representation
- Reachable zones from a selected hub
- BFS traversal with hop levels
- DFS cycle detection
- Shortest path and delivery time calculation
- Hash table insertion, search, deletion, resizing, and collision handling
- Heap insertion, extraction, and priority updates
- Integrated test across graph, hash table, and heap modules
- Sorting test results for 100, 500, and 1000 delivery records

## Key Features

- Modular system design
- Custom implementation of major data structures
- Graph-based delivery network modelling
- Customer management using hash tables
- Priority-based parcel handling using max heap
- Sorting and reporting using quick sort and merge sort
- CSV import and export functionality
- Independent module testing
- Integrated system testing
- Algorithm complexity analysis

## Skills Demonstrated

This project demonstrates:

- Python programming
- Data structures and algorithms
- Object-oriented programming
- Modular software design
- Algorithm complexity analysis
- Graph traversal
- Shortest path calculation
- Hash table design
- Heap-based priority queue implementation
- Sorting algorithm implementation
- CSV-based testing and reporting

## Limitations

Some limitations of the project include:

- The parcel priority score formula is simplified and may not fully reflect real-world logistics priority rules.
- The graph implementation avoids built-in Python data structures, which makes the code more complex but supports the learning objective.
- Dijkstra’s algorithm uses linked-list scanning, resulting in O(V²) complexity rather than a more optimised priority queue approach.
- The logistics network is based on a simplified simulated structure rather than a real-world road network.
- External CSV files were used for testing and demonstration purposes.

## Future Improvements

Possible improvements include:

- Implementing Dijkstra’s algorithm with a priority queue for better efficiency.
- Adding real map or road network data.
- Improving the parcel priority formula using more realistic logistics factors.
- Adding a user interface or command-line menu.
- Adding automated unit tests for each module.
- Improving visualisation of delivery routes and priority queues.

## Repository Contents

This repository may include:

- Python source code files
- Module test files
- CSV input files
- CSV output files
- Sample screenshots
- Technical report
- README documentation

## Note

This project was developed for academic and portfolio purposes to demonstrate practical understanding of data structures, algorithms, modular programming, and algorithmic performance analysis.
