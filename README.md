# iQuHACK_2021_QuAK
### Nurse Scheduling Problem using Discrete Quadratic Model
### Team QuACK
### Problem Statement
We performed DQM (Discrete Quadratic Model) implementation of Nurse Scheduling Model developed by Ikeda, Nakamura and Humble (INH) using hybrid quantum annealing. 
For the INH Nurse Scheduling problem we had to assign nurses to shifts complying by three constraints: 

1)	hard nurse constraint: no consecutive shifts for a nurse
2)	hard shift constraint: at least one nurse present for one shift
3)	soft nurse constraint: nurses should have “approximately” even schedule (the “softness” of the constraint is due to the approximation) 

The nurse scheduling problem is a Non-deterministic Polynomial Time Hard Problem. (NP-hard problem)
This read me contains a holistic overview of the problem and the approaches we took to solve it. 

### Discrete Quadratic Model (DQM)
The DQM is a quadratic polynomial which takes discrete variables such as {yellow, red, green} or {6.77, 3.45, 33.44}. Using DQM, encoding for discrete variable problems has become easier. The change from binary variables of BQM to discrete variables opens the door to solve new types of problems using a quantum computer. 
The DQM function can be represented by a general form of:

$ E(\bf{x})
= \sum_{i=1}^N \sum_{u=1}^{n_i} a_{i,u} x_{i,u}
+ \sum_{i=1}^N \sum_{j=i+1}^N \sum_{u=1}^{n_i} \sum_{v=1}^{n_j} b_{i,j,u,v} x_{i,u} x_{j,v}
+ c $
