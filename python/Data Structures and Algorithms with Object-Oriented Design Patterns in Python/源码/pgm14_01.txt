#
# This file contains the Python code from Program 14.1 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm14_01.txt
#
class Solution(Object):

    def __init__(self):
        super(Solution, self).__init__()

    def getIsFeasible(self):
        pass
    getIsFeasible = abstractmethod(getIsFeasible)

    isFeasible = property(
        fget = lambda self: self.getIsFeasible())

    def getIsComplete(self):
        pass
    getIsComplete = abstractmethod(getIsComplete)

    isComplete = property(
        fget = lambda self: self.getIsComplete())

    def getObjective(self):
        pass
    getObjective = abstractmethod(getObjective)

    objective = property(
        fget = lambda self: self.getObjective())

    def getBound(self):
        pass
    getBound = abstractmethod(getBound)

    bound = property(
        fget = lambda self: self.getBound())

    def getSuccessors(self):
        pass
    getSuccessors = abstractmethod(getSuccessors)

    successors = property(
        fget = lambda self: self.getSuccessors())
