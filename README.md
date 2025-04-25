# 🧭 Optimal Autonomous 3D Terrain Navigation
A simulation framework to compare and evaluate the performance of four classical search algorithms—A*, Uniform Cost Search (UCS), Greedy Best-First Search, and Rapidly-Exploring Random Tree (RRT)—for autonomous navigation over realistic 3D terrains modeled using hexagonal grid geometry.

---

## 📌 Overview

This project investigates the effectiveness of graph-based and sampling-based algorithms for navigating through procedurally generated 3D terrains. Terrain data is generated using **Perlin Noise**, and each hexagonal cell contains an elevation value influencing the movement cost. The goal is to identify the most efficient algorithm for real-time autonomous navigation across complex environments.

---

## 🔍 Algorithms Implemented

- **A\***  
  Combines cost-so-far `g(n)` and heuristic `h(n)` to find near-optimal paths efficiently.  
- **Uniform Cost Search (UCS)**  
  Explores the lowest cumulative cost path without heuristic guidance.  
- **Greedy Best-First Search**  
  Explores nodes with the lowest heuristic value, focusing on speed over optimality.  
- **Rapidly-Exploring Random Tree (RRT)**  
  Random sampling-based approach suitable for dynamic and high-dimensional spaces.

---

## 🗺️ Terrain Generation

- **Grid Model**: Hexagonal grid for realistic navigation.
- **Elevation**: Generated using Perlin noise to simulate realistic hills and valleys.
- **Movement Cost**: Depends on elevation change between neighboring hex cells:
  - Uphill → Penalty applied
  - Downhill → Bonus applied

---

## 📊 Evaluation Metrics

### For Algorithms:
- ✅ **Path Length**: Number of steps in the generated path.
- 💰 **Path Cost**: Accumulated terrain-aware movement cost.
- ⏱ **Computation Time**: Time taken to find the path.
- 🌲 **Nodes Expanded**: Number of states visited.

### For Terrains:
- 🏔️ **Elevation Range**: Difference between min and max elevation.
- 📈 **Elevation Variance**: Measures surface roughness.
- 🚧 **Obstacle Density**: % of grid cells exceeding an elevation threshold.
- 🔁 **Local Roughness**: Average elevation change between neighbors.

---

### Results Summary
Algorithm | Avg. Path Cost | Avg. Time (ms) | Nodes Expanded
A* | ⭐ Balanced | Fast | Low
UCS | Optimal | Slow | Very High
Greedy | Fastest | Lowest | Very Low
RRT | Robust | High | Moderate

---

### Authors
- Hrithiq Gupta
- Arnav Sahu

---
 
### License
This project is licensed under the MIT License. See the LICENSE file for details.
