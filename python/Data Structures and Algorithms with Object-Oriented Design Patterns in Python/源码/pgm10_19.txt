#
# This file contains the Python code from Program 10.19 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm10_19.txt
#
class BTree(MWayTree):

    def __init__(self, m):
        super(BTree, self).__init__(m)
        self._parent = None

    def attachSubtree(self, i, t):
        self._subtree[i] = t
        t._parent = self

    # ...
