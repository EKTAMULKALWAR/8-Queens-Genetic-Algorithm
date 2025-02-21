1. Introduction
1.1 Purpose of the Report
This report presents the application of an Evolutionary Algorithm (EA) to solve the 8-Queens problem. The objective is to find a configuration of eight queens on an 8×8 chessboard where no two queens attack each other.

1.2 Overview of the 8-Queens Problem
The 8-Queens problem is a classic constraint satisfaction and optimization problem. The goal is to place 8 queens on a chessboard so that no two queens share the same row, column, or diagonal.

1.3 Evolutionary Algorithms (EA) in Optimization
Evolutionary Algorithms (EA) are inspired by natural selection and operate using selection, crossover, and mutation to optimize solutions iteratively. The 8-Queens problem is well suited for EA because it is a complex combinatorial optimization problem with a large search space.

2. Methodology
2.1 Evolutionary Algorithm Approach
The EA used for solving the 8-Queens problem follows these steps:
Initialization: Generate a population of 100 random board configurations.
Fitness Evaluation: Calculate the number of conflicts (attacking queens) for each board.
Selection: Use Tournament Selection to pick parents.
Crossover: Use Order Crossover (OX) to combine parent genes.
Mutation: Swap two random positions in a board with a given probability (pm).
Survivor Selection: Merge offspring with the existing population and keep the best solutions.
Termination: Stop if an optimal solution is found or after 100 generations.
2.2 Problem Representation
Each board is represented as a permutation of numbers [1,2,3,4,5,6,7,8], where the ith index represents the row, and the value represents the column position of a queen.

3. Results and Analysis
the graph displays the result.

3.1 Mutation Probability = 60%
Found an optimal solution in 2 generations.
Initial average fitness = 5.12 (high number of conflicts).
Quickly dropped to 2.93, then reached 0 (no conflicts).
✅ Best Solution Found:
[3, 7, 2, 8, 5, 1, 4, 6]
Interpretation:
Lower mutation led to a quick convergence but may not always escape local optima.
3.2 Mutation Probability = 80%
Required 9 generations to find an optimal solution.
The fitness gradually decreased:
5.17 → 3.07 → 2.46 → 2.05 → 1.07 → 0
More exploration resulted in a steady improvement over generations.
 Best Solution Found:
[6, 3, 1, 7, 5, 8, 2, 4]
Interpretation:
Higher mutation increases diversity but requires more generations to refine solutions.

3.3 Mutation Probability = 100%
Required 3 generations to find an optimal solution.
Fitness evolution: 4.77 → 3.09 → 2.59 → 0
Faster convergence compared to 80% mutation.
✅ Best Solution Found:
[8, 2, 5, 3, 1, 7, 4, 6]
Interpretation:
Maximum mutation provides high exploration but can sometimes disrupt good solutions.
Despite randomness, it quickly converged to an optimal state.


4. Visualization & Analysis

Mutation 60% (🔵): Steep initial drop, quick solution but might not always generalize well.
Mutation 80% (🟠): Gradual decline, requiring more generations.
Mutation 100% (🟢): Fast convergence, but more unstable.
      Best Fitness vs Average Fitness Over Generations
Best Fitness (dashed lines) shows how the best solution evolved.
Average Fitness (solid lines) represents population-wide improvements.
Conclusion from Graph
Higher mutation rates (80%–100%) allow for deeper exploration but may slow down refinement.
Lower mutation (60%) quickly finds a solution but may struggle in more complex setups.
Mutation 100% converged in just 3 generations, but randomness can sometimes be risky.

5. Conclusion
Evolutionary Algorithms successfully solve the 8-Queens problem.
Mutation plays a key role in balancing exploration and exploitation.
Best mutation rate: 80% (found a solution while maintaining diversity).
Future Work:
Dynamic mutation rates (adjust mutation over time).
Hybrid methods (combine Genetic Algorithm with local search for refinement).

6. References
Russell, S.J., & Norvig, P. (2016). Artificial Intelligence: A Modern Approach. Pearson.
Eiben, A.E., & Smith, J.E. (2015). Introduction to Evolutionary Computing. Springer-Verlag.
https://colab.research.google.com/drive/1Lsh6g0A-aj5tmz9_kTsrHh0MEwZMLeug?usp=sharing


