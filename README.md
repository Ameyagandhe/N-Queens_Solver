# Topic : N-Queens Problem Solver
This repository contains a set of Python implementations for solving the N-Queens problem using various Constraint Satisfaction Problem (CSP) algorithms. The N-Queens problem is a classic combinatorial problem that consists of placing N queens on an N x N chessboard such that no two queens threaten each other. In other words, no two queens should share the same row, column, or diagonal.
## Algorithms
The following CSP algorithms have been implemented in this repository to solve the N-Queens problem:
### 1. Backtracking: 
A depth-first search algorithm that incrementally builds a solution by placing queens row by row while checking if the current partial solution is safe. If not, the algorithm backtracks to the previous row and tries a different column. [n_queens_backtracking.py](https://github.com/Ameyagandhe/INFO_550_FINAL_PROJECT/blob/main/n_queens_backtracking.py.ipynb)
### 2. Forward Checking: 
An extension of the backtracking algorithm that maintains a set of domain values (possible column placements) for each unassigned row. When a queen is placed, the algorithm updates the domains of the remaining rows and prunes any placements that would result in a conflict. [n_queens_forward_checking.py](https://github.com/Ameyagandhe/INFO_550_FINAL_PROJECT/blob/main/n_queens_forward_checking.py.ipynb)
### 3. MRV Heuristic: 
The Minimum Remaining Values (MRV) heuristic is a variable ordering strategy that selects the row with the fewest legal column placements, helping to reduce the search space. [n_queens_mrv.py](https://github.com/Ameyagandhe/INFO_550_FINAL_PROJECT/blob/main/n_queens_mrv.py.ipynb)
### 4. LCV Heuristic: 
The Least Constraining Value (LCV) heuristic is a value ordering strategy that sorts the possible column placements based on the number of conflicts they cause in the remaining rows, prioritizing the least constraining placements. [n_queens_lcv.py](https://github.com/Ameyagandhe/INFO_550_FINAL_PROJECT/blob/main/n_queens_lcv.py.ipynb)
### 5. Local Search: 
A stochastic search algorithm that starts with a random placement of queens and iteratively improves the solution by swapping queens' positions within the same column to minimize the number of conflicts. [n_queens_local_search.py](https://github.com/Ameyagandhe/INFO_550_FINAL_PROJECT/blob/main/n_queens_local_search.py.ipynb)
## Usage
To run the algorithms, first clone the repository and navigate to the project folder:

git clone https://github.com/Ameyagandhe/n-queens-solver.git

cd n-queens-solver

Next, make sure you have Python 3.x installed and run the desired algorithm:

python n_queens_backtracking.py

python n_queens_forward_checking.py

python n_queens_mrv.py

python n_queens_lcv.py

python n_queens_local_search.py

You can change the size of the board by modifying the n variable in the corresponding script.

## Performance
The performance of each algorithm may vary depending on the size of the board and the specific problem instance. In general, backtracking and forward checking are more efficient for smaller problem sizes, while local search can be effective for larger boards. However, local search does not guarantee finding a solution, whereas backtracking, forward checking, and the MRV and LCV heuristics will always find a solution if one exists.

## License
This project is licensed under the MIT License. See the [LICENSE.md](https://github.com/Ameyagandhe/INFO_550_FINAL_PROJECT/blob/main/LICENSE) file for more information.
