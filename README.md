Course CSc 220 Algorithms Fall Semester 2016
Homework Project 3
Given 11/23/2016, Due 12/14/2016
Write a function that implements Kruskal’s algorithm to compute the minimum spanning
tree of a graph.
int MST(int n, int *cost, int limit);
Here n is the number of vertices (labelled 0 to n−1), and cost is integer array cost[n][n].
A cost value of limit or above indicates an edge that can not be used. Your function
returns the cost of the minimum spanning tree.
You first create an array of all edges of cost below limit. You use the function qsort
from the C standard library to sort it in sequence of increasing cost. Then you create
the set union data sttructure, which is an array of size n for the index of the next vertex,
if it exists, and another array of size n for the rank of each vertex. Using this structure,
you execute Kruskal’s algorithm, and return the total length of the minimum spanning
tree.