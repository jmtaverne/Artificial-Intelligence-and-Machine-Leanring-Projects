# Diagonal Sudoku Solver

This project is part of the Udacity - Artificial Intelligence Nanodegree. 
You can check out the solution in the file: solution-master.py


## Synopsis

In this project, you will extend the Sudoku-solving agent developed in the classroom lectures to solve diagonal Sudoku puzzles and implement a new constraint strategy called "naked twins". A diagonal Sudoku puzzle is identical to traditional Sudoku puzzles with the added constraint that the boxes on the two main diagonals of the board must also contain the digits 1-9 in each cell (just like the rows, columns, and 3x3 blocks). The naked twins strategy says that if you have two or more unallocated boxes in a unit and there are only two digits that can go in those two boxes, then those two digits can be eliminated from the possible assignments of all other boxes in the same unit.

## Quickstart Guide

YOU ONLY NEED TO WRITE CODE IN solution.py.

Follow the instructions in the classroom lesson to install and configure the aind Anaconda environment which includes several important packages that are used for the project. OS X or Unix/Linux users can activate the aind environment by running the following (Windows users simply run activate aind):

$ source activate aind

You can run a small set of test cases using the local test suite.

(aind)$ python -m unittest -v

Copy your code from the classroom for the search and basic strategies, then add the diagonal units at the top of the solutions.py file and complete the naked_twins() function. Pseudocode for the naked_twins() function is available here.

Run the test suite again to check your progress. Once you pass all the test cases in the local test suite, you can submit the project to run more comprehensive tests with the remote test suite:

(aind)$ udacity submit

You can run the code with visualization (see the last section of the readme for more information)

(aind)$ python solution.py


## Instructions

You must complete the required functions in the 'solution.py' file (copy in code from the classroom where indicated, and add or extend with new code as described below). The test_solution.py file includes a few unit tests for local testing, but the primary mechanism for testing your code is the Udacity Project Assistant command line utility described in the next section.

YOU SHOULD EXPECT TO MODIFY OR WRITE YOUR OWN UNIT TESTS AS PART OF COMPLETING THIS PROJECT. There is no requirement to write test cases, but the Project Assistant test suite is not shared with students so writing your own tests may be necessary to find and resolve any errors that arise there.

Add the two new diagonal units to the unitlist at the top of solution.py. Re-run the local tests with python -m unittest to confirm your solution.

Copy your code from the classroom for the eliminate(), only_choice(), reduce_puzzle(), and search() into the corresponding functions in the solution.py file.

Implement the naked_twins() function (see the pseudocode here for help), and update reduce_puzzle() to call it (along with the other existing strategies). Re-run the local tests with python -m unittest -v to confirm your solution.

Run the remote tests with udacity submit to confirm your solution. If any of the remote test cases fail, use the feedback to write your own local test cases for debugging.


## Visualization

Note: The pygame library is required to visualize your solution -- however, the pygame module can be troublesome to install and configure. It should be installed by default with the AIND conda environment, but it is not reliable across all operating systems or versions. Please refer to the pygame documentation here, or discuss among your peers in the slack group if you need help.

Running python solution.py will automatically attempt to visualize your solution, but you mustuse the provided assign_value function (defined in utils.py) to track the puzzle solution progress for reconstruction during visuzalization.
