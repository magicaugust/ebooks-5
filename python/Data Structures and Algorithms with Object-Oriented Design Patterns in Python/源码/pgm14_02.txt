#
# This file contains the Python code from Program 14.2 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm14_02.txt
#
class Solver(Object):

    def __init__(self):
        super(Solver, self).__init__()
        self._bestSolution = None
        self._bestObjective = sys.maxint

    def search(self, initial):
        pass
    search = abstractmethod(search)

    def solve(self, initial):
        assert isinstance(initial, Solution)
        self._bestSolution = None
        self._bestObjective = sys.maxint
        self.search(initial)
        return self._bestSolution

    def updateBest(self, solution):
        if solution.isComplete and solution.isFeasible and \
                solution.objective < self._bestObjective:
            self._bestSolution = solution
            self._bestObjective = solution.objective

    # ...
