#
# This file contains the Python code from Program 9.14 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm09_14.txt
#
class NaryTree(Tree):

    def getSubtree(self, i):
        if self.isEmpty:
            raise StateError
        return self._subtree[i]

    def attachSubtree(self, i, t):
        if self.isEmpty or not self._subtree[i].isEmpty:
            raise StateError
        self._subtree[i] = t

    def detachSubtree(self, i):
        if self.isEmpty:
            raise StateError
        result = self._subtree[i]
        self._subtree[i] = NaryTree(degree)
        return result

    # ...
