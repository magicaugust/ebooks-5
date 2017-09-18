#
# This file contains the Python code from Program 14.3 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm14_03.txt
#
class DepthFirstSolver(Solver):

    def __init__(self):
        super(DepthFirstSolver, self).__init__()

    def search(self, current):
        if current.isComplete:
            self.updateBest(current)
        else:
            for successor in current.successors:
                self.search(successor)
