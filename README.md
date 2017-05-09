# Artificial Intelligence Nanodegree
## Introductory Project: Diagonal Sudoku Solver

# Question 1 (Naked Twins)
Q: How do we use constraint propagation to solve the naked twins problem?  
Constraint propagation is the idea of applying a constraint as many times as possible until a solution is obtained, or the constraint can no longer be applied to refine the solution.

Naked twins is the strategy we apply to reduce the number of possible solution per box. The strategy is to identify a pair of boxes belonging to the same set of peers that have the same 2 numbers as possibilities, and eleminate these two numbers from all the boxes that have these two boxes as peers. First we identify all boxes that have only 2 elements. Next we identify which boxes among these have the same elements to get naked twins. Once we get the naked twins, we remove the corresponding digits from all the boxes that are peers to both the twins.

# Question 2 (Diagonal Sudoku)
Q: How do we use constraint propagation to solve the diagonal sudoku problem?  
If we think of the diagonals as additional units to the game, changing a value in one of the boxes in the diagonals will immediately propagate constraints into the box's three other units (row, column, square). Once this is done, all the diagonal entries will have the corresponding diagonal entries as their peers. This will result in not accepting solutions that do not satisfy the diagonal constraint.
### Install

This project requires **Python 3**.

We recommend students install [Anaconda](https://www.continuum.io/downloads), a pre-packaged Python distribution that contains all of the necessary libraries and software for this project. 
Please try using the environment we provided in the Anaconda lesson of the Nanodegree.

##### Optional: Pygame

Optionally, you can also install pygame if you want to see your visualization. If you've followed our instructions for setting up our conda environment, you should be all set.

If not, please see how to download pygame [here](http://www.pygame.org/download.shtml).

### Code

* `solution.py` - You'll fill this in as part of your solution.
* `solution_test.py` - Do not modify this. You can test your solution by running `python solution_test.py`.
* `PySudoku.py` - Do not modify this. This is code for visualizing your solution.
* `visualize.py` - Do not modify this. This is code for visualizing your solution.

### Visualizing

To visualize your solution, please only assign values to the values_dict using the ```assign_values``` function provided in solution.py

### Submission
Before submitting your solution to a reviewer, you are required to submit your project to Udacity's Project Assistant, which will provide some initial feedback.  

The setup is simple.  If you have not installed the client tool already, then you may do so with the command `pip install udacity-pa`.  

To submit your code to the project assistant, run `udacity submit` from within the top-level directory of this project.  You will be prompted for a username and password.  If you login using google or facebook, visit [this link](https://project-assistant.udacity.com/auth_tokens/jwt_login for alternate login instructions.

This process will create a zipfile in your top-level directory named sudoku-<id>.zip.  This is the file that you should submit to the Udacity reviews system.

