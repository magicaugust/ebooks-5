#
# This file contains the Python code from Program 10.13 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm10_13.txt
#
class MWayTree(SearchTree):

    def __init__(self, m):
	assert m > 2
        super(MWayTree, self).__init__()
        self._key = Array(m - 1, 1)
        self._subtree = Array(m)

    def getM(self):
        return len(self._subtree)

    m = property(
        fget = lambda self: self.getM())

    # ...
