
# Integer Programming Approach to the Travelling Salesperson Problem (TSP)

This project explores a variation of the Travelling Salesperson Problem (TSP) using integer linear programming. It was developed as part of the Open University's MST374 course on Mathematical and Computational Modelling. Some of the code used in this project was provided by the Open University as part of the assignment materials and extended to meet the project objectives.

## 🎯 Project Focus: Automating Constraint Generation

The **main goal** of this project was to develop and implement a method for **automating the process of adding subtour elimination constraints** (from question 1, part b iii forward in the solution) in the ad hoc TSP approach. The project first manually identifies and resolvs disjoint subtours, then it introduces a dynamic algorithm that detects subtours and automatically inserts the necessary constraints during the optimization loop.

This automated ad hoc approach was then compared against a traditional general method (MTZ formulation) in terms of performance and scalability.

## 🧠 Methodology Overview

### 1. **Ad Hoc Automated Constraint Approach (Main Contribution)**
- Detects disjoint subtours during optimization.
- Automatically generates and adds additional constraints to eliminate them.
- Reduces the need for manual intervention and improves solver usability.

### 2. **General (MTZ) Constraint Approach**
- Uses Miller–Tucker–Zemlin constraints.
- Prevents subtours by adding all necessary constraints at once.
- Often slower due to the large number of constraints introduced upfront.

## ⚖️ Performance Comparison

### Evaluation
- Both approaches were tested on datasets with city counts ranging from N = 2 to 24.
- Performance was measured using `%timeit` and plotted.
- Visual comparisons and benchmark plots were generated.

### Key Insights
- The **automated ad hoc approach** is significantly more efficient for N ≤ 15.
- The **MTZ method** becomes computationally expensive as N increases.
- Automation made the ad hoc method more scalable and practical for larger N.

## 🧪 Heuristic Strategies for Further Optimization

The project also investigated ways to **reduce the number of constraints** required in the automated approach, including:

- Starting from a point in the densest cluster (using kmeans2).
- Starting from the most isolated point.
- Choosing a midpoint between cluster centers.
- Manual visual selection based on spatial distribution.

### Outcome
- Most heuristics had inconsistent impact or worsened performance.
- **Manual visual selection** in dense regions proved most effective, particularly for N ≥ 20.

## 🛠️ Technologies

- Python 3
- NumPy
- Pandas
- SciPy (`linprog`)
- Matplotlib
- SciPy's `kmeans2` for clustering


This project was submitted as part of MST374 at the Open University. It focuses on building real-world modelling and algorithmic skills through computational optimization.

## 👤 Author

Ruslan Gyurov — BSc (Hons) Computing and Mathematics

