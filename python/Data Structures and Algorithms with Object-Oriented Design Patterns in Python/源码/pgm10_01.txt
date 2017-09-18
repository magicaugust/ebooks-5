#
# This file contains the Python code from Program 10.1 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm10_01.txt
#
class SearchTree(Tree, SearchableContainer):

    def __init__(self):
        super(SearchTree, self).__init__()

    def getMin(self):
        pass
    getMin = abstractmethod(getMin)

    min = property(
        fget = lambda self: self.getMin())

    def getMax(self):
        pass
    getMax = abstractmethod(getMax)

    max = property(
        fget = lambda self: self.getMax())
