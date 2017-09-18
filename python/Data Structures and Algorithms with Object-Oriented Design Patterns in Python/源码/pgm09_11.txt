#
# This file contains the Python code from Program 9.11 of
# "Data Structures and Algorithms
# with Object-Oriented Design Patterns in Python"
# by Bruno R. Preiss.
#
# Copyright (c) 2003 by Bruno R. Preiss, P.Eng.  All rights reserved.
#
# http://www.brpreiss.com/books/opus7/programs/pgm09_11.txt
#
class GeneralTree(Tree):

    def getKey(self):
        return self._key

    def getSubtree(self, i):
        if i < 0 or i >= self._degree:
            raise IndexError
        ptr = self._list.head
        for j in xrange(i):
            ptr = ptr.next
        return ptr.datum

    def attachSubtree(self, t):
        self._list.append(t)
        self._degree += 1

    def detachSubtree(self, t):
        self._list.extract(t)
        self._degree -= 1
        return t
    # ...
