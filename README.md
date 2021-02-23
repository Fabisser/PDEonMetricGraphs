# PDEonMetricGraphs
A Jupyter notebook program designed so that the user can create a metric graph and apply a PDE (Heat or Wave) on it.

This code, written in Jupyter notebook, simulates the heat or wave equation on a metric graph. The code has 6 parts. To start the user has to define the graph, which is done by describing the vertices and edges of the graph. We prescribe a length, a discretization and initial conditions  to the edges, and boundary conditions to the vertices.

We create a "Graph" class to store all the information about the graph, split into Graph.Nodes for the vertices and Graph.Edges for the edges. The user then has to create, in the function addjunctCoords, the graph in 2d plane, assigning the nodes and edges (x_1,x_2) values.

The function GraphLaplacian creates the Laplacian of the graph. We then calculate the solution in calcSol using (in this case) the RK4 method, which finally gives us a solution W which contains the solution for every edge for every timestep. The last function PlotGraph places the solution of one edge in 3d space, such that we can plot each edge as it's own function in 3d space later.

We finally calculate the solution using the functions just defined, and finally use a grapher to plot each edge as a function in 3d space through time.

Included at the end is a plot of the Laplacian to understand what it looks like for the user created graph.
