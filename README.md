# Memory Manager – Python Simulator

## Description

This project is a **memory management simulator** developed in Python. It divides memory into fixed-size blocks and allows process allocation and deallocation using different memory allocation algorithms such as **First Fit, Best Fit, and Worst Fit**.

The graphical user interface (GUI) was implemented using **Tkinter**, providing a visual representation of memory blocks, including occupied and free spaces.

In addition, the project was extended by modifying the `memoryManager.py` and `gui.py` files to implement **FIFO (First In First Out)** and **LRU (Least Recently Used)** page replacement algorithms.

---

## Features

### Fixed Memory Block Division

* Total memory size: **128 KB**
* Block size: **2 KB**
* Each process occupies whole blocks, even if the requested size is smaller than a full block.

---

## Supported Allocation Algorithms

### Memory Allocation Algorithms

* **First Fit**
  Allocates the process in the first continuous free space large enough to fit it.

* **Best Fit**
  Allocates the process in the smallest available continuous free space that can contain it.

* **Worst Fit**
  Allocates the process in the largest available continuous free space.

---

## Page Replacement Algorithms

### FIFO (First In First Out)

* Removes the oldest allocated process from memory when there is not enough space available.
* Processes are managed using a queue structure.

### LRU (Least Recently Used)

* Removes the least recently used process from memory when memory becomes full.
* Uses timestamps to track process usage.

---

## Process Deallocation

* Processes can be manually deallocated from memory through the program.

---

## GUI Visualization (Tkinter)

* Free blocks are displayed in **green**
* Occupied blocks are displayed in **red**
* Process names are shown inside occupied blocks
* Buttons are available for:

  * First Fit
  * Best Fit
  * Worst Fit
  * FIFO
  * LRU
  * Deallocate

---

## Terminal Display

The `display()` function prints the current memory status in the terminal, showing which blocks are free and which are occupied.

---

## Project Structure

```bash
memory-manager/
│
├── block.py           # Block class representing each memory block
├── memoryManager.py   # MemoryManager class with allocation/deallocation logic
├── gui.py             # Tkinter graphical user interface
└── main.py            # Main script to run the simulator
```

---

## How to Use

### 1. Clone the Repository

```bash
git clone https://github.com/Yuri-Diego/memory-manager.git
cd memory-manager
```

### 2. Run the Simulator

Use Python 3.13 or higher:

```bash
python main.py
```

### 3. GUI Visualization

The GUI window will open showing the memory state:

* Green blocks → Free memory
* Red blocks → Occupied memory

---

## Important Notes

* **Partial Allocation:**
  Each process occupies complete memory blocks. If a process does not fully use a block, the remaining space in that block cannot be shared with another process.

* **Manual Deallocation:**
  Currently, processes must be manually deallocated using:

```python id="kxh9c0"
deallocate(process)
```

---

## Dependencies

* Python 3.13 or higher
* Tkinter (usually included with standard Python installation)

---

## Future Improvements

* Implement automatic deallocation when memory becomes full.
* Add more interactive GUI controls for allocation and deallocation.
* Improve the visualization by centering process names inside larger blocks.
* Add different colors for different processes instead of a single occupied color.
