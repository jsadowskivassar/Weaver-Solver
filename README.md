# Weaver-Solver

## Overview:

Solves word ladder game using a given word list. Utilizes **Breadth First Search (BFS)**, treating each word as a node and visiting adjacent nodes (words that are within one letter of initial word) until the target word is reached. Includes function to return all words one letter away from given word and function to return shortest path between two words.

## Algorithmic Approach
This program utilizes a **Breadth-First Search (BFS)** to guarantee the shortest possible path.
* **Graph Theory Mechanics:** Each valid word acts as a node. Edges exist between nodes that differ by exactly one character. 
* **Queue Operations:** Implements `collections.deque` for highly efficient First-In-First-Out (FIFO) state management during the level-by-level traversal.
* **Cycle Prevention:** Utilizes a `visited` hash set to prevent redundant loops and drastically reduce time complexity.
* **Scalability:** Built with scalability in mind to dynamically handle dictionaries of any string length, scaling cleanly beyond standard 4-letter puzzle constraints.

## Tech Stack
* **Language:** Python
* **Core Concepts:** Graph Traversal, Queue Data Structures

## Usage
The solver requires a loaded list of dictionary words (e.g., `weaver_list` included in repository). You can find all words within one letter of a particular word by calling the `possible_words` function or the shortest path between two words by calling the `path()` function.

```python
#Example execution determining all adjacent words to 'spot'
print(possible_words("spot"))

#Output: ['scot', 'shot', 'slot', 'snot', 'soot', 'spat', 'spit', 'stot', 'swot']

#Example execution determining the shortest path from 'shot' to 'boat'
print(path('shot', 'boat'))

#Output: ['shot', 'soot', 'boot', 'boat']
