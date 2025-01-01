# Release Notes for v0.2

## Overview
The v0.2 release focuses on code refactoring, enhanced functionality, and program performance analysis. Major improvements include the reorganization of code into multiple header and source files, the addition of exception handling, and significant optimization tasks for handling large datasets efficiently. The release also introduces features for categorizing and sorting student data based on their final scores.

---

## New Features

### 1. **Code Refactoring**
- Code has been modularized:
  - All methods and data types are now organized into `.h` (header) and `.cpp` (implementation) files.
  - Improved readability, maintainability, and scalability.
- Introduced exception handling to manage issues such as:
  - Non-existent files during file input operations.
  - Out-of-bound access in arrays or containers.
  
### 2. **Random Student Data Generation**
- Added functionality to generate student data files with varying sizes:
  - 10,000 records.
  - 100,000 records.
  - 1,000,000 records.
  - 10,000,000 records.
- Generated student names and surnames follow the format:
  - Name1 Surname1
  - Name2 Surname2
  
### 3. **Student Sorting and Splitting**
- Students are categorized into two groups based on their final scores:
  - `Failed`: Final score < 5.0.
  - `Passed`: Final score ≥ 5.0.
- Results are saved to two separate output files for each group.

### 4. **Performance Analysis**
- Measured and logged the execution time of critical operations:
  - File reading.
  - Sorting and categorizing students.
  - Splitting data into two groups.
  - Writing sorted data to output files.
- Test cases use datasets of varying sizes (1,000 to 10,000,000 records).

### 5. **Alternative Containers Implementation**
- Introduced versions of the code utilizing:
  - `std::vector` (base implementation).
  - `std::list`.
  - `std::deque`.
- Performed and compared performance analyses for all three container types across five test datasets.

---

## Implementation Details

### Directory Structure
The updated project now follows a modular structure:
```
project-root/
├── include/
│   ├── person.h
│   ├── file_utils.h
│   ├── performance_utils.h
│
├── src/
│   ├── person.cpp
│   ├── file_utils.cpp
│   ├── performance_utils.cpp
│   ├── main.cpp
│
├── data/
│   ├── students10000.txt
│   ├── students100000.txt
│   ├── students1000000.txt
│   ├── students10000000.txt
│
├── output/
│   ├── passed_students.txt
│   ├── failed_students.txt
│
├── README.md
└── Makefile
```

### Exception Handling
- Examples of handled exceptions:
  - FileNotFoundError: If an input file does not exist, the program displays an appropriate error message and exits gracefully.
  - OutOfRangeError: Prevents invalid access in containers.

### Performance Metrics
The program measures the duration of each critical operation using:
- `std::chrono` library for time measurement.

---

## Testing and Results

### Test Files
- Five test files generated with random data:
  - 1,000 records.
  - 10,000 records.
  - 100,000 records.
  - 1,000,000 records.
  - 10,000,000 records.

### Performance Results
#### With `std::vector`
| Dataset Size | File Read Time | Sorting Time | Splitting Time | Write Time | Total Time |
|--------------|----------------|--------------|----------------|------------|------------|
| 1,000        | xx ms          | xx ms        | xx ms          | xx ms      | xx ms      |
| 10,000       | xx ms          | xx ms        | xx ms          | xx ms      | xx ms      |
| 100,000      | xx ms          | xx ms        | xx ms          | xx ms      | xx ms      |
| 1,000,000    | xx ms          | xx ms        | xx ms          | xx ms      | xx ms      |
| 10,000,000   | xx ms          | xx ms        | xx ms          | xx ms      | xx ms      |

#### Comparisons (Vector vs. List vs. Deque)
| Container Type | Operation             | Average Execution Time (ms) |
|----------------|-----------------------|------------------------------|
| `std::vector`  | File Read             | xxx                          |
|                | Sorting               | xxx                          |
|                | Splitting             | xxx                          |
|                | Write                | xxx                          |
| `std::list`    | File Read             | xxx                          |
|                | Sorting               | xxx                          |
|                | Splitting             | xxx                          |
|                | Write                | xxx                          |
| `std::deque`   | File Read             | xxx                          |
|                | Sorting               | xxx                          |
|                | Splitting             | xxx                          |
|                | Write                | xxx                          |

---

## Future Tasks
For the upcoming release `v0.25`:
1. Extend all implemented functionality using `std::list` and `std::deque`.
2. Conduct detailed performance analysis with varying dataset sizes.
3. Document performance trade-offs between the three container types.
4. Publish results and new release.

---

## How to Build and Run
### Build Instructions
1. Clone the repository.
   ```bash
   git clone <repository-url>
   cd project-root
   ```
2. Build the program:
   ```bash
   make
   ```

### Run Instructions
1. Execute the program:
   ```bash
   ./main
   ```
2. Provide input file paths when prompted.

---

## Authors and Contributions
This project is developed by [Your Name/Team Name]. Contributions include modularized code design, efficient data management, and performance optimization.

---

## Changelog
### v0.2
- Introduced modular code structure.
- Added exception handling.
- Implemented large dataset processing and categorization.
- Performed program performance analysis with `std::vector`.

### Upcoming v0.25
- Alternative container implementations (`std::list`, `std::deque`).
- Extended performance analysis.

