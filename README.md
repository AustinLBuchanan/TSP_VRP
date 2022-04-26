# TSP_VRP
Example codes for the traveling salesman problem (TSP) and vehicle routing problem (VRP). All codes are written in Python, handle graphs using NetworkX, and solve integer programs using the Gurobi optimizer. 

Helpful references: 
1. [The traveling salesman problem: A case study in local optimization](https://scholar.google.com/scholar?cluster=8249601619393406923&hl=en&as_sdt=0,37) by Johnson and McGeoch.
2. [The Vehicle Routing Problem](https://scholar.google.com/scholar?cluster=5139244580018150315&hl=en&as_sdt=0,37) edited by Toth and Vigo.
3. [Video lecture by Bill Cook](https://youtu.be/5VjphFYQKj8)
4. [Bill Cook's TSP page](http://www.math.uwaterloo.ca/tsp/)

Also see a [Python interface for the LKH heuristic](https://github.com/fikisipi/elkai) and [simple test](https://github.com/AustinLBuchanan/LKH_test/blob/main/lkh-test.ipynb).


## Heuristics
1. [nearest_neighbor_heuristic](https://github.com/AustinLBuchanan/TSP_VRP/blob/main/nearest_neighbor_heuristic.ipynb)
   - Generates a random 20-city TSP instance in the plane
   - Visualizes the instance using NetworkX
   - Implements the nearest neighbor heuristic
   - Visualizes the solution using NetworkX
2. [two_opt_heuristic](https://github.com/AustinLBuchanan/TSP_VRP/blob/main/two_opt_heuristic.ipynb)
   - Generates a random 20-city TSP instance in the plane
   - Visualizes the instance using NetworkX
   - Implements the 2-opt local search heuristic
   - Visualizes each intermediate solution using NetworkX

## Approximation Algorithms
1. [two_approximation_algorithm](https://github.com/AustinLBuchanan/TSP_VRP/blob/main/two_approximation_algorithm.ipynb)
   - Generates a random 20-city TSP instance in the plane
   - Visualizes the instance using NetworkX
   - Finds a minimum spanning tree using NetworkX
   - Replaces each undirected edge with oppositely directed edges
   - Finds an Eulerian cycle using NetworkX
   - Removes repeated nodes to generate a 2-approximate solution
   - Visualizes the solution using NetworkX
2. [Christofides_algorithm](https://github.com/AustinLBuchanan/TSP_VRP/blob/main/Christofides_algorithm.ipynb)
   - Generates a random 20-city TSP instance in the plane
   - Visualizes the instance using NetworkX
   - Finds a minimum spanning tree using NetworkX
   - Finds a minimum cost perfect matching over the odd-degree nodes of the tree using NetworkX
   - Finds an Eulerian cycle of (tree edges) + (matching edges) using NetworkX
   - Removes repeated nodes to generate a 1.5-approximate solution
   - Visualizes the solution using NetworkX

## Optimization Models
1. [DFJ_model](https://github.com/AustinLBuchanan/TSP_VRP/blob/main/DFJ_model.ipynb)
   - Generates a random 20-city TSP instance in the plane
   - Visualizes the instance using NetworkX
   - Solves the 2-matching relaxation using Gurobi
   - Visualizes the 2-matching solution using NetworkX
   - Adds violated subtour elimination constraints (in an iterative fashion)
   - Visualizes the solution using NetworkX
2. [DFJ_model_with_callbacks](https://github.com/AustinLBuchanan/TSP_VRP/blob/main/DFJ_model_with_callbacks.ipynb)
   - Generates a random 20-city TSP instance in the plane
   - Visualizes the instance using NetworkX
   - Solves the DFJ model using Gurobi
   - Adds violated subtour elimination constraints in a callback
   - Visualizes the solution using NetworkX
3. [MTZ_model](https://github.com/AustinLBuchanan/TSP_VRP/blob/main/MTZ_model.ipynb)
   - Generates a random 20-city TSP instance in the plane
   - Visualizes the instance using NetworkX
   - Solves the assignment relaxation using Gurobi
   - Visualizes the assignment solution using NetworkX
   - Adds Miller-Tucker-Zemlin constraints and re-solves using Gurobi
   - Visualizes the solution using NetworkX
4. [MTZ_CVRP_model](https://github.com/AustinLBuchanan/TSP_VRP/blob/main/MTZ_CVRP_model.ipynb)
   - Generates a random 20-city, 4-vehicle CVRP instance in the plane
   - Visualizes the instance using NetworkX
   - Solves an assignment relaxation using Gurobi
   - Visualizes the assignment solution using NetworkX
   - Adds the CVRP version of the Miller-Tucker-Zemlin constraints and re-solves using Gurobi
   - Visualizes the solution using NetworkX
5. [RCI_CVRP_model](https://github.com/AustinLBuchanan/TSP_VRP/blob/main/RCI_CVRP_model.ipynb)
   - Generates a random 20-city, 4-vehicle CVRP instance in the plane
   - Visualizes the instance using NetworkX
   - Adds violated rounded capacity inequalities (or subtour elimination constraints) in a callback
   - Visualizes the solution using NetworkX
