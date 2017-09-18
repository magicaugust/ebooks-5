#
# This file contains the Python code from Program 14.5 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm14_05.txt
#
class DepthFirstBranchAndBoundSolver(Solver):

    def __init__(self):
        super(DepthFirstBranchAndBoundSolver, self).__init__()

    def search(self, current):
        if current.isComplete:
            self.updateBest(current)
        else:
            for successor in current.successors:
                if successor.isFeasible and \
                        successor.bound < self._bestObjective:
                    self.search(successor)
