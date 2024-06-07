# PACE2024
This repository contains our, Kristoffer Sandvang and Mateusz Filipowski, solution for the [PACE 2024 challenge](https://pacechallenge.org/2024/) on the heuristic track. 
We have particpated as a part of writing our Bachelor's thesis. 

## Description
This solver uses the median and barycenter heuristic to solve the one-sided crossing minimization problem, which involves arranging nodes of one layer in a two-layered bipartite graph. Furthermore, it uses the permutation tie breaking method to handle ties in both heuristics if the time limit allows it. 
Otherwise it will use the orginal barycenter heuristic, and use the median heuristic where the barycenter heuristic is used to break ties. It then selects the heuristic that has produced a permutation of B that produces the fewest crossings and writes the ordering of B.

## How to compile and run
The solver can be compiled by first typing 
```
cmake -G "MinGW Makefiles" ./src
``` 
and then 
```
make
``` 

Once the solver has been compiled you can run it by:
```
$ ./PACE2024.exe < graph.gr
``` 
Or if you prefer to write the graph in the terminal:
```
$ ./PACE2024.exe
```
Here it is important that your graph follows the [exact input format specified by PACE](https://pacechallenge.org/2024/io/).