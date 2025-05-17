

# 🎨 Graph Coloring Problem (Backtracking)

This Python program solves the **Graph Coloring** problem using **backtracking**. It assigns colors to graph vertices such that no two adjacent vertices share the same color.

---

## 📌 Description

* Takes user input for:

  * Number of vertices
  * Number of edges
  * Number of available colors
  * Edge list (as vertex pairs)
* Uses recursive backtracking to find a valid coloring.
* If successful, prints the color assignment for each vertex.

---



## 🧠 Key Functions

* `is_safe(graph, color_assignment, vertex, color)`
  Checks if a color can be assigned to a vertex without conflict.

* `graph_coloring_util(graph, k, color_assignment, vertex)`
  Recursive function that tries to assign colors.

---

## 📤 Sample Output

```
Graph Coloring Problem

Coloring Possible with 3 Colors  
Color Assignment: [1, 2, 3, 1]
```

---

## ❗ Notes

* Vertices are assumed to be **0-indexed**.
* Works only for **undirected graphs**.
* May not be optimal for large graphs due to the backtracking nature.



