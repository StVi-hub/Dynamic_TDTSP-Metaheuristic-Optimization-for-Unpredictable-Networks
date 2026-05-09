Dynamic-TDTSP: Metaheuristic Optimization for Unpredictable Networks

Project Overview

This project addresses a specialized variant of the Traveling Salesman Problem: the Time-Dependent Traveling Salesman Problem (TDTSP) with Dynamic Road Blockages. In real-world logistics, travel costs are rarely constant; they fluctuate based on traffic patterns and unexpected infrastructure failures.

This repository provides a complete framework for modeling these complexities and solving them using advanced metaheuristic algorithms, specifically designed for resilient supply chain management and autonomous routing.

Key Features

Time-Dependent Cost Matrices: Travel costs evolve dynamically as the agent moves through the network.

Stochastic Road Blockages: Simulates real-world disruptions (accidents, construction) via dynamic edge unavailability.

Mathematical Rigor: Full formalization of the objective function and constraints using Linear Programming (LP) standards.

Hybrid Metaheuristics: Implementation and comparison of Genetic Algorithms (GA) and Ant Colony Optimization (ACO).

Complexity Analysis: Formal proof of the problem's membership in the NP-Hard class.

Mathematical Formulation

The problem is modeled as a graph $G = (V, A)$ where the cost function $c_{i,j}(t)$ depends on the departure time $t$ from node $i$.

Objective Function

Minimize the total arrival time at the final destination:


$$\min Z = \sum_{(i,j) \in A} \sum_{t \in T} c_{i,j}(t) \cdot x_{i,j,t}$$

Implementation & Algorithms

The project utilizes Python and the PuLP library for exact modeling, alongside custom implementations of:

Genetic Algorithm (GA):

Custom crossover operators for permutation preservation.

Adaptive mutation rates to avoid local optima.

Ant Colony Optimization (ACO):

Pheromone update rules modified for time-dependent costs.

State-dependent heuristic desirability.

Performance Evaluation

OFAT (One-Factor-At-a-Time) Analysis: Systematic hyperparameter tuning.

Lower Bound Calculation: Comparison against theoretical minima to assess the optimality gap.

Tech Stack

Language: Python 3.11.9

Modeling: PuLP (Linear Programming)

Analysis: NumPy, Matplotlib, Pandas